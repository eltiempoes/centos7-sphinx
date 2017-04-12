# Docker CentOS image with Sphinx open source search engine

This Docker image is intended to be used as a general Sphinx search engine server

# How to use it

You should provide the sphinx configuration to make the server work:

`docker run -d -v /home/user/sphinx/sample.conf:/etc/sphinx/sphinx.conf eltiempoes/centos7-sphinx`

If you need a DB to generate the indexes you have to provide a link to the database container:

`docker run -d -v /home/user/sphinx/sample.conf:/etc/sphinx/sphinx.conf --link db:db eltiempoes/centos7-sphinx`

After doing that, you can change set the database host in sphinx configuration to `db`
