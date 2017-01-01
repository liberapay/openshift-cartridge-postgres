A Postgres 9.4.10 Cartridge for OpenShift v2.

Note: this cartridge does NOT run in an Auto-Scale app configuration.

To install it run this command:

    rhc cartridge add -a APP_NAME http://cartreflect-claytondev.rhcloud.com/github/liberapay/openshift-cartridge-postgres

Don't forget to make regular backups of your databases using `pg_dump`, and be
careful not to delete or alter the `$OPENSHIFT_DATA_DIR/postgres/` directory
that stores them.

To test the installation run this commands:

    pg_ctl status -D $OPENSHIFT_PG_DATA_DIR

    psql -d template1 -U $PGUSER

To restart the cartridge run this command:

    rhc cartridge restart liberapay-postgres-9.4.5 --app APP_NAME