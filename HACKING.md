# Release procedure
* Documentation
  * Make sure the doc is up to date (See Documentation generation)
  * In the wikidoc branch, copy dev to VERSION
* update VERSION
* dune-release tag $(cat VERSION)
* dune-release distrib
* dune-release publish distrib
* dune-release opam pkg
* dune-release opam submit

# Documentation generation
* make doc
* make installdoc
* cd _wikidoc
* git diff # review diff
* git commit -am "sync doc"
* git push origin wikidoc
