Description
===========

DirDuster is a web directory bruteforcing tool similar to DirBuster.
It allows you to quickly check for the presence of files or directories in
order to detect potential flaws in the way the web server is configured.

Visit `my blog`__ for a complete presentation!

.. _purrfect: http://breakpoint.purrfect.fr/article/dirduster_presentation.html

__ purrfect_

Why DirDuster?
==============

The main tool used for this task is DirBuster_ which is written in Java and
uses a graphical interface. This makes it hard enough to use for me to prefer
writting another tool with a more proper interface.

.. _DirBuster: https://www.owasp.org/index.php/Category:OWASP_DirBuster_Project

There also exist dirb_ but it doesn't allow the user to specify the number of
threads which means a massive slowdown on my machine which wasn't acceptable
anymore.

.. _dirb: http://dirb.sourceforge.net/

Documentation
=============

::

    Fast brute force of web directories

    Usage: dirduster [options] -f FILE URL...

    Arguments:
        URL     Urls to bruteforce

    Options:
        -h, --help             Print this help and exit
        -v, --version          Print the version and exit

        -a, --auth CREDS       Basic authentication in the format login:password
        -c, --cookies COOKIES  User-defined cookies in the format Cookie=Value
                               Use multiple times for multiple cookies
        -d, --directories      Identify and search directories
        -f, --file FILE        Entries file
        -H, --headers HEADERS  User-defined headers in the format Header=Value
                               Use multiple times for multiple headers
        -i, --ignore CODES     List of comma separated invalid codes
        -I, --list-ignore      List the default invalid codes
        -m, --method           HTTP method to use; defaults to GET
        -p, --proxy PROXY_URL  Proxy url; may contain authentication data
        -s, --single-pass      Disable recursion on findings
        -t, --threads NUM      Number of threads to use, default is 10
        -u, --user-agent UA    Set custom user agent
        -x, --exclude REGEX    Exclude pages matching REGEX

Building
========

Use dub:

::

    dub build -b release

License
=======

This program is under the GPLv3 License.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.

Contact
=======

::

    Main developper: Cédric Picard
    Email:           cpicard@purrfect.fr
