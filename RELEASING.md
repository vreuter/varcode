# Releasing Varcode

This document explains what do once your [Pull Request](https://www.atlassian.com/git/tutorials/making-a-pull-request/) has been reviewed and all final changes applied. Now you're ready merge your branch into master and release it to the world:

1. Merge your branch into master.

2. Assign a version to the release you are preparing. Varcode uses [versioneer](https://github.com/warner/python-versioneer), so rather
than explicitly editing `__version__` variable in the code you must instead tag the release with your new version number (e.g. `git tag v1.2.3`).

3. Run `git push --tags`.

4. After the Varcode unit tests complete successfully on Travis then the latest version
of the code (with the version specified above) will be pushed to [PyPI](https://pypi.python.org/pypi) automatically. If you're curious about how automatic deployment is achieved, see our [Travis configuration](https://github.com/hammerlab/varcode/blob/master/.travis.yml#L51).