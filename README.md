melancholia
===========

[![Mini-ci Build Status](http://maicolino-lb-apps-442062849.sa-east-1.elb.amazonaws.com:8888/repositories/maiconio/melancholia/refs/heads/master/badge)](http://maicolino-lb-apps-442062849.sa-east-1.elb.amazonaws.com:8888/repositories/maiconio/melancholia/refs/heads/master/badge)

Melancholia enshrines all triumph.

Prepare melancholia user
---------------------

Create melancholia user

```
CREATE ROLE melancholia LOGIN SUPERUSER;
```
Set melancholia password

```
ALTER USER melancholia WITH PASSWORD 'm1e2l3a4';
```

Prepare your database
---------------------

Melancholia is using PostgreSQL.

Create your database

```
createdb melancholia
```

Import the *data.sql* file

```
psql melancholia -f data.sql
```

If you feel like testing
------------------------

```
createdb melancholia_test
```

Also import the *data.sql* file

```
psql melancholia_test -f data.sql
```

And go inside the models (the only one tested so far) folder and run:

```
go test
```

Done ;)
