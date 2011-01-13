git-deploy
==========

Install
-------
Download and install the gem:

    $ wget --no-check-certificate https://github.com/downloads/scottbnel/git-deploy/git-deploy-0.0.1.gem
    $ gem install git-deploy
    
Usage
-----
In the root of the Git repository you wish to deploy, create a `deploy.yml` file like so:

    scheme: sftp
    host: example.com
    username: user
    password: pass
    path: path/to/deployment
    
    exclude:
      - .gitignore
      - deploy.yml
      
Then, to deploy the HEAD revision of the repository, run:

    $ git deploy