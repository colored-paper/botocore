Contributing
============

We work hard to provide a high-quality and useful SDK, and we greatly value
feedback and contributions from our community. Whether it's a new feature,
correction, or additional documentation, we welcome your pull requests. Please
submit any `issues <https://github.com/boto/botocore/issues>`__
or `pull requests <https://github.com/boto/botocore/pulls>`__ through GitHub.

This document contains guidelines for contributing code and filing issues.

Contributing Code
-----------------

The list below are guidelines to use when submitting pull requests.
These are the same set of guidelines that the core contributors use
when submitting changes, and we ask the same of all community
contributions as well:

* The SDK is released under the
  `Apache license <http://aws.amazon.com/apache2.0/>`__.
  Any code you submit will be released under that license.
* We maintain a high percentage of code coverage in our unit tests.  As
  a general rule of thumb, code changes should not lower the overall
  code coverage percentage for the project.  To help with this,
  we use `coveralls <https://coveralls.io/r/boto/botocore>`__, which will
  comment on changes in code coverage for every pull request.
  In practice, this means that every bug fix and feature addition should
  include unit tests.
* If you identify an issue with the JSON service descriptions,
  such as ``botocore/data/aws/s3/2006-03-01/service-2.json``, please submit an
  `issue <https://github.com/boto/botocore/issues>`__ so we can get it
  fixed upstream.
* Changes to paginators, waiters, and endpoints are also generated upstream based on our internal knowledge of the AWS services.
  These include any of the  following files in ``botocore/data/``:
  
  * ``_endpoints.json``
  * ``*.paginators-1.json``
  * ``*.waiters-2.json``

  If you identify an issue with these files, such as a missing paginator or waiter, please submit an
  `issue <https://github.com/boto/botocore/issues>`__ so we can get it fixed upstream.
*  We do accept, and encourage, changes to the ``botocore/data/_retry.json`` file.
* Code should follow `pep 8 <https://www.python.org/dev/peps/pep-0008/>`__,
  although if you are modifying an existing module, it is more important
  for the code to be consistent if there are any discrepancies.
* Code must work on ``python3.6`` and higher.
* Botocore is cross platform and code must work on at least linux, Windows,
  and Mac OS X.
* If you would like to implement support for a significant feature that is not
  yet available in botocore, please talk to us beforehand to avoid any duplication
  of effort.  You can file an
  `issue <https://github.com/boto/botocore/issues>`__
  to discuss the feature request further.


Reporting An Issue/Feature
--------------------------

*  Check to see if there's an existing issue/pull request for the
   bug/feature. All issues are at
   https://github.com/boto/botocore/issues and pull reqs are at
   https://github.com/boto/botocore/pulls.
*  If there isn't an existing issue there, please file an issue. The
   ideal report includes:

   * A description of the problem/suggestion.
   * A code sample that demonstrates the issue.
   * Including the versions of your:

     * python interpreter
     * OS
     * botocore (accessible via ``botocore.__version__``)
     * optionally any other python dependencies involved
