*django-geoexplorer* allows you to use `GeoExplorer <http://opengeo.org>`_
in your `Django <https://www.djangoproject.com>`_ projects.

This is just packaging work for the great opengeo suite client sdk.

The releases will be done based on the suite releases or a git hash will be appended to the package name before publishing to pypi in the following way:

3.0.1.devXXXXX where XXXXX is the git hash and the url to the source code can be constructed as follows:

https://github.com/opengeo/suite/tree/XXXXX

=======
INSTALL
=======

::

    pip install django-geoexplorer

=====
USAGE
=====

* Add ``geoexplorer`` to your ``INSTALLED_APPS``


=======
AUTHORS
=======

* Ariel Núñez <http://ingenieroariel.com>

==========
DEVELOPERS
==========

::

    git clone http://github.com/GeoNode/suite.git
    cd suite
    git submodule update --init
    cd ../
    git clone http://github.com/GeoNode/django-geoxplorer.git
    cp -R suite/geoexplorer/target/geoexplorer/WEB-INF/app/static/* django-geoexplorer/geoexplorer/static/
    cd django-geoexplorer
    git add geoexplorer/static
    vim setup.py  # update the version number
    git add setup.py
    git commit -m "Commit committed, a new release was needed because the other one was old."
    git push origin master
    python setup.py sdist upload

=======
LICENSE
=======

* Lesser GNU Public License
* OpenGeo Suite License - GPL
