A Postgres 9.4.10 Cartridge for OpenShift v2.

Note: this cartridge does NOT run in an Auto-Scale app configuration.

To install it run this command:

    rhc cartridge add http://cartreflect-claytondev.rhcloud.com/github/liberapay/openshift-cartridge-postgres

Don't forget to make regular backups of your databases using `pg_dump`, and be
careful not to delete or alter the `$OPENSHIFT_DATA_DIR/postgres/` directory
that stores them.
