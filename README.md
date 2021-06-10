DESCRIPTION :
	
	A monothread HTTP server, based on nginx, written in C++98, and compliant with
	RFC 7230 to 7235.
	It uses select() for multiplexing.
	
It supports the following headers :
	
	Accept-Charsets
	Accept-Language
	Allow
	Authorization
	Content-Language
	Content-Length
	Content-Location
	Content-Type


BUILD :
	
	$> make

USAGE :
	
	$> ./webserv [config.conf]

SERVER CONFIGURATION :

	The configuration file follows nginx's server blocks's basic syntax with
	a few simplifications :
	- There are no core contexts (http, main, events) declarations.
	  The whole configuration file is assumed by the server to be an http
	  context. You can only declare 'server' blocks and their nested 'location'
	  blocks.
	- Only supports the following directives :
		- server_name
		- listen
		- root
		- index
		- error_page
		- cli_max_size
		- allow
		- autoindex
		- alias
		- cgi_pass

Credits :

[Charlie Armstrong](https://github.com/charMstr)
Loic Buckwell (lfalkau)
[Lambert Spiess](https://github.com/lambertspiess)
