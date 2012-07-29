MageSh(ell) v0.2
================================================================================

Magento Utility Shell Script
--------------------------------------------------------------------------------
> Ryan Shaltry, http://ryanshaltry.com
> Joe Constant, http://joeconstant.me

OVERVIEW
--------------------------------------------------------------------------------
> PHP Script for utility-based operations on a Magento instance, including
> cache flushes, indexing, MySQL client connection, log file viewing, and
> configuration settings.

INSTALL
--------------------------------------------------------------------------------
1. Place the magesh PHP script into a directory in the $PATH
2. Verify magesh script is executable (755)
3. Verify the location of the PHP interpreter on line 1 of script
4. [Optional] Install AWS PHP SDK (To use aws functions)

        sudo pear channel-discover pear.amazonwebservices.com
        sudo pear install aws/sdk

USAGE
--------------------------------------------------------------------------------
> $ magesh COMMAND [METHOD]
>
> The magesh command should be run from a Magento directory instance, or
> can be loaded one level up ('project' level) from any of the following
> directories (listed in order of precedence): www, public_html, magento
>
> NOTE: Run magesh with no options to view usage information.

BASIC EXAMPLES
--------------------------------------------------------------------------------
<pre>$ magesh db</pre>
<pre>$ magesh cache flush</pre>
<pre>$ magesh indexer catalogsearch_fulltext</pre>

STDIN BOOTSTRAPPING
--------------------------------------------------------------------------------
> The magesh script accepts input on STDIN for bootstrapping Magento scripts.
> Utility scripts no longer require bootstrapping libraries or includes, e.g.:
<pre>$ cat scripts/create-report.php | magesh</pre>

PREFERENCES
--------------------------------------------------------------------------------
> The ~/.magesh file has the following available options (defaults shown):
> * debug  = 1
> * colors = 0
> * AWS_KEY = (Amazon Web Services Key. Found in the AWS Security Credentials)
> * AWS_SECRET = (Amazon Web Services Secret Key. Found in the AWS Security Credentials)

LICENSE
--------------------------------------------------------------------------------
>
> This program is free software: you can redistribute it and/or modify
> it under the terms of the GNU General Public License as published by
> the Free Software Foundation, either version 3 of the License, or
> (at your option) any later version.
>
> This program is distributed in the hope that it will be useful,
> but WITHOUT ANY WARRANTY; without even the implied warranty of
> MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
> GNU General Public License for more details.
>
> You should have received a copy of the GNU General Public License
> along with this program.  If not, see <http://www.gnu.org/licenses/>.
