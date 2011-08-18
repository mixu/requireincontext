# RequireInContext

Allows you to do a require() with a custom context.

# Installing:

    npm install requireincontext

# Using:

Useful for emulating a browser environment in Node:

    var requireInContext = require('requireincontext');
    var myclient = requireInContext('./myclient.js', {
      window: {},
      io: require('socket.io')
    });

Or for specifying mock objects for running tests:

    var requireInContext = require('requireincontext');
    var mycode = requireInContext('./mycode.js', {
      mydependency: require('./dependency_mock.js')
    });

