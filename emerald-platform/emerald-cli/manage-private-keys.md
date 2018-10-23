# Manage Private Keys

## Private Key Management <a id="private-key-management"></a>

### Show all available accounts <a id="_show_all_available_accounts"></a>

```text
$ emerald account list
```

### Exclude an account from the showing in the list <a id="_exclude_an_account_from_the_showing_in_the_list"></a>

```text
$ emerald account hide  0x0e7c045110b8dbf29765047380898919c5cb56f4
```

To undo in the future:

```text
$ emerald account unhide --all
```

### Create new account <a id="_create_new_account"></a>

```text
$ emerald account new \
    --security-level=high \
    --name="Test account" \
    --description="Some description" \
    < echo "secret passphrase"
```

### Show private key <a id="_show_private_key"></a>

```text
$ emerald account strip 0x0e7c045110b8dbf29765047380898919c5cb56f4 < echo "secret passphrase"
```

### Change private key passphrase <a id="_change_private_key_passphrase"></a>

```text
$ emerald account strip 0x0e7c045110b8dbf29765047380898919c5cb56f4 < echo "old passphrase" \
$ emerald account new --raw < echo "new passphrase"
```

### Change account name <a id="_change_account_name"></a>

```text
$ emerald account update \
    0x0e7c045110b8dbf29765047380898919c5cb56f4 \
    --name="New name" \
    --description="A new description"
```

### Import keyfile <a id="_import_keyfile"></a>

Import content of whole folder:

```text
$ emerald account import --all <path_to_files>
```

or single keyfile:

```text
$ emerald account import <path_to_file>
```

If keyfile already exist in a storage, import will be ignore.

To override existing Keyfile, use `-f | --force` option:

```text
$ emerald account import --force <path_to_file>
```

### Export keyfile <a id="_export_keyfile"></a>

Export all keyfiles into directory:

```text
$ emerald account export --all <path_to_export_dir>
```

or single keyfile for selected &lt;address&gt;:

```text
$ emerald account export <address> <path_to_export_dir>
```

