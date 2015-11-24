# python-rackspace-auth
keystoneauth plugin for Rackspace's authentication service

[![Build Status](https://travis-ci.org/rackerlabs/python-rackspace-auth.svg)](https://travis-ci.org/rackerlabs/python-rackspace-auth)

This package provides plugins to [keystoneauth1](https://pypi.python.org/pypi/keystoneauth1/), the OpenStack Keystone authentication library, for Rackspace's supported authentication methods: API key, password, and token.

### Example Usage

```python
from rackspaceauth import v2
from keystoneauth1 import session

auth = v2.APIKey(username="Mayor McCheese",
                 key="OMGCHEESEISGREAT")
                     
sess = session.Session(auth=auth)
sess.get_token()
```