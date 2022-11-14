# Dropbox-v2-PHP-SDK
PHP SDK for Dropbox built with the v2 API

*Last update: 2/23/2018*

## Installation
- Include in composer.json this git repo
"repositories": [{
        "type": "git",
        "url": "https://github.com/pietos/Dropbox-v2-PHP-SDK.git"
 }],
- Include the following requirement in composer.json
  "pietos/dropbox-v2-php-sdk": "dev-master",

## Documentation
- Documentation will be improved in the future. Check out [Example.php](Example.php) for basic usage.
- [Dropbox API documentation](https://www.dropbox.com/developers/documentation/http/documentation)
- You can look in the appropriate file to see usage.

### Version 1.1.7
- Added option to `files->upload()` and `files->download()` to upload/download raw data respectively.
- Please see `sdk/Dropbox/Files.php` for usage.
----------------------

**Bolded** items will not be implemented.

### auth
- [x] /token/from_oauth1
- [x] /token/revoke

### file_properties
- [x] /properties/add
- [x] /properties/overwrite
- [x] /properties/remove
- [x] /properties/search
- [x] /properties/update
- [x] /templates/add_for_user
- [x] /templates/get_for_user
- [x] /templates/list_for_user
- [x] /templates/update_for_user

### file_requests
- [x] /create
- [x] /get
- [x] /list
- [x] /update

### files
- [ ] **/alpha/get_metadata** *PREVIEW*
- [ ] **/alpha/upload** *PREVIEW*
- [x] /copy *DEPRECATED BY /copy_v2*
- [x] /copy_batch
- [x] /copy_batch/check
- [x] /copy_reference/get
- [x] /copy_reference/save
- [x] /copy_v2
- [x] /create_folder *DEPRECATED BY /create_folder_v2*
- [x] /create_folder_v2
- [x] /delete *DEPRECATED BY /delete_v2*
- [x] /delete_batch
- [x] /delete_batch/check
- [x] /delete_v2
- [x] /download
- [x] /get_metadata
- [x] /get_preview
- [x] /get_temporary_link
- [x] /get_thumbnail
- [x] /list_folder
- [x] /list_folder/continue
- [x] /list_folder/get_latest_cursor
- [x] /list_folder/longpoll
- [x] /list_revisions
- [x] /move *DEPRECATED BY /move_v2*
- [x] /move_batch
- [x] /move_batch/check
- [x] /move_v2
- [x] /permanently_delete
- [ ] **/properties/add** *PREVIEW*
- [ ] **/properties/overwrite** *PREVIEW*
- [ ] **/properties/remove** *PREVIEW*
- [ ] **/properties/template/get** *PREVIEW*
- [ ] **/properties/update** *PREVIEW*
- [x] /restore
- [x] /save_url
- [x] /save_url/check_job_status
- [x] /search
- [x] /upload
- [x] /upload_session/append *DEPRECATED BY /upload_session/append_v2*
- [x] /upload_session/append_v2
- [x] /upload_session/finish
- [x] /upload_session/finish_batch
- [x] /upload_session/finish_batch/check
- [x] /upload_session/start

### paper
- [x] /docs/archive
- [x] /docs/create
- [x] /docs/download
- [x] /docs/folder_users/list
- [x] /docs/folder_users/list/continue
- [x] /docs/get_folder_info
- [x] /docs/list
- [x] /docs/list/continue
- [x] /docs/permanently_delete
- [x] /docs/sharing_policy/get
- [x] /docs/sharing_policy/set
- [x] /docs/users/add
- [x] /docs/users/list
- [x] /docs/users/list/continue
- [x] /docs/users/remove

### sharing
- [x] /add_file_member
- [x] /add_folder_member
- [x] /change_file_member_access *DEPRECATED BY /update_file_member*
- [x] /check_job_status
- [x] /check_remove_member_job_status
- [x] /check_share_job_status
- [x] /create_shared_link *DEPRECATED BY /create_shared_link_with_settings*
- [x] /create_shared_link_with_settings
- [x] /get_file_metadata
- [x] /get_file_metadata/batch
- [x] /get_folder_metadata
- [x] /get_shared_link_file
- [x] /get_shared_link_metadata
- [x] /get_shared_links *DEPRECATED BY /list_shared_links*
- [x] /list_file_members
- [x] /list_file_members/batch
- [x] /list_file_members/continue
- [x] /list_folder_members
- [x] /list_folder_members/continue
- [x] /list_folders
- [x] /list_folders/continue
- [x] /list_mountable_folders
- [x] /list_mountable_folders/continue
- [x] /list_received_files
- [x] /list_received_files/continue
- [x] /list_shared_links
- [x] /modify_shared_link_settings
- [x] /mount_folder
- [x] /relinquish_file_membership
- [x] /relinquish_folder_membership
- [x] /remove_file_member *DEPRECATED BY /remove_file_member_2*
- [x] /remove_file_member_2
- [x] /remove_folder_member
- [x] /revoke_shared_link
- [x] /share_folder
- [x] /transfer_folder
- [x] /unmount_folder
- [x] /unshare_file
- [x] /unshare_folder
- [x] /update_file_member
- [x] /update_folder_member
- [x] /update_folder_policy

### users
- [x] /get_account
- [x] /get_account_batch
- [x] /get_current_account
- [x] /get_space_usage
------------------

## Additional Functions

### `Dropbox/Files->getThumbnailSize($size)`
Converts standard thumbnail sizes into pixel values usable by Dropbox functions, i.e. `'thumb' => 'w32h32'`

## Troubleshooting

### Local Machine SSL Certificate Issues
Dropbox requires that you have a valid SSL certificate. If you are facing an issue where the SDK is always returning `null` or `false`, this could be the issue. Try following the solution to [this StackOverflow question](https://stackoverflow.com/questions/28858351/php-ssl-certificate-error-unable-to-get-local-issuer-certificate).
