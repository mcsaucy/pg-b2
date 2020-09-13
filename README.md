#`pg-b2`

Takes a `pg_dump` from a postgresql database and uploads it to Backblaze B2.


## Usage

`pg-b2 bucket_name table_name [ filename_prefix ]`

For example, `pg-b2 k3s_dumps k3s hourly/` will take a dump of the `k3s` table
and upload that dump to the `hourly/k3s.pgdump` file in the `k3s_dumps` bucket.

The dump is temporarily stored in `$HOME/.pgb2_scratch/` (or
`/tmp/.pgb2_scratch` if `$HOME` is empty). This location can be overwritten by
via the `$PGB2_SCRATCH_DIR` environment variable.
