1.  clone
2.  npm install
3.  database - postgresql
    - psql postgres
    - CREATE ROLE electron_release_server_user ENCRYPTED PASSWORD <<pwd here>> LOGIN;
    - CREATE DATABASE electron_release_server OWNER "electron_release_server_user";
    - CREATE DATABASE electron_release_server_sessions OWNER "electron_release_server_user";
    - psql electron_release_server_sessions < ./sql/sails-pg-session-support.sql electron_release_server_user;
