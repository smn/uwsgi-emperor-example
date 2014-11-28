uWSGI Emperor Example
=====================

Start uWSGI in Emperor mode with two Django app vassals::

        $ virtualenv ve
        $ source ve/bin/activate
        (ve)$ pip install -r requirements.txt
        (ve)$ ./run-wsgi.sh

Start Nginx::

        $ nginx -c `pwd`/nginx.conf

Issue a request with curl to see the app being started automatically
& stopped when idling::

        $ curl -XGET http://localhost:9000/

