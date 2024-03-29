# Wildcard Policy Examples

This example demonstrates various wildcard policies for KV secrets in the `kv/` path.

The Terraform files create a user, KVv1 mount, and policy that grants varying levels of access to secrets in the `kv/` path.

## Example 4A

1. Log in to Vault as `user4a` with password "changeme"
    "user4a" will be able to write within specific subfolder of the root path and in some cases additional restrictions are applied.
    >
    > ```bash
    > vault login -method=userpass username=user4a
    > Password (will be hidden):
    > Success! You are now authenticated. The token information displayed below
    > is already stored in the token helper. You do NOT need to run "vault login"
    > again. Future Vault requests will automatically use this token.
    > ```

2. Write a secret in `folder1` (this will succeed)
    >
    > ```bash
    > vault write kv/folder1/my_secret password=P@ssw0rd!
    > ```

3. Attempt to write a secret in folder2 (this will fail)
    >
    > ```bash
    > vault write kv/folder2/secret password=P@ssw0rd!
    > ```

4. Attempt to write a secret in folder2 prefixed with the letter "p" (this will succeed)
    >
    > ```bash
    > vault write kv/folder2/prefix_secret password=P@ssw0rd!
    > ```

5. Attempt to write a secret "my_secret" in any folder (this will succeed)
    >
    > ```bash
    > vault write kv/folder4/my_secret password=P@ssw0rd!
    > ```

6. Attempt to write a secret "my_secret" in "folder5" (this will fail)
    >
    > ```bash
    > vault write kv/folder5/my_secret password=P@ssw0rd!
    > ```

## Example 4B

1. Log in to Vault as `user4b` with password "changeme"
    "user4b" will be able to write the secret "my_secret" in any subfolder of the KV root.
    >
    > ```bash
    > vault login -method=userpass username=user4b
    > Password (will be hidden):
    > Success! You are now authenticated. The token information displayed below
    > is already stored in the token helper. You do NOT need to run "vault login"
    > again. Future Vault requests will automatically use this token.
    > ```

2. Attempt to write a secret "my_secret" in "folder5" (this will succeed)
    >
    > ```bash
    > vault write kv/folder5/my_secret password=P@ssw0rd!
    > ```

3. Attempt to write a secret in the root path (this will fail)
    >
    > ```bash
    > vault write kv/my_secret password=P@ssw0rd!
    > ```

4. Attempt to write a secret in any subfolder of the root path (this will succeed)
    >
    > ```bash
    > vault write kv/my_secret password=P@ssw0rd!
    > ```

5. Attempt to write a secret within two subfolders (this will fail)
    >
    > ```bash
    > vault write kv/folder/subfolder/my_secret password=P@ssw0rd!
    > ```

## Example 4C

1. Log in to Vault as `user4c` with password "changeme"
    "user4c" will be able to write any secret in any subfolder of the KV root but will be unable to write directly to the root path.
    >
    > ```bash
    > vault login -method=userpass username=user4c
    > Password (will be hidden):
    > Success! You are now authenticated. The token information displayed below
    > is already stored in the token helper. You do NOT need to run "vault login"
    > again. Future Vault requests will automatically use this token.
    > ```

2. Attempt to write a secret within one subfolder (this will succeed)
    >
    > ```bash
    > vault write kv/folder/my_secret password=P@ssw0rd!
    > ```

3. Attempt to write a secret within two subfolders (this will succeed)
    >
    > ```bash
    > vault write kv/folder/subfolder/my_secret password=P@ssw0rd!
    > ```

4. Attempt to write a secret within the root path (this will fail)
    >
    > ```bash
    > vault write kv/my_secret password=P@ssw0rd!
    > ```

## Observations

* `*` is a glob character and can only be used at the end of paths
* `+` is a component specific wildcard and can only be surrounded by `/` (i.e. `"+/.."`, or "`../+`, or `../+/..`)
* Most specific paths win. A path with `+` at the beginning is less specific than a path with a particular mount defined.

## Policies

View the policies in Vault:

* user4a_policy
* user4b_policy
* user4c_policy
* user4d_policy
