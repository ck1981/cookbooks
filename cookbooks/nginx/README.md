# DESCRIPTION:

Installs nginx from package OR source code and sets up configuration handling similar to Debian's Apache2 scripts.

# REQUIREMENTS:

## Cookbooks:

* build-essential (for nginx::source)

## Platform:

Debian or Ubuntu though may work where 'build-essential' works, but other platforms are untested.

# ATTRIBUTES:

* version - sets the version to install.
* install_path - for nginx::source, sets the --prefix installation.
* src_binary - for nginx::source, sets the binary location.
* dir - configuration dir.
* log_dir - where logs go.
* user - user to run as.
* binary - path to nginx binary.
* configure_flags - for nginx::source, the flags to use for compilation.
** gzip** - configure the gzip module.
* keepalive - whether to use keepalive.
* keepalive_timeout
* worker_processes - number of workers to spawn.
* worker_connections - number of connections per worker.
* server_names_hash_bucket_size

# USAGE:

Provides two ways to install and configure nginx.

* Install via native package (nginx::default)
* Install via compiled source (nginx::source)

Both recipes implement configuration handling similar to the Debian Apache2 site enable/disable.

There's some redundancy in that the config handling hasn't been separated from the installation method (yet), so use only one of the recipes.

# LICENSE and AUTHOR:

Author:: Joshua Timberman (<joshua@opscode.com>)
Author:: Adam Jacob (<adam@opscode.com>)
Author:: AJ Christensen (<aj@opscode.com>)

Copyright:: 2008-2010, Opscode, Inc

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
