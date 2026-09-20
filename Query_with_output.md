1. **ffuf -u http://10.48.179.191/FUZZ -w /usr/share/seclists/Discovery/Web-Content/big.txt:FUZZ -mc 200**

________________________________________________

 :: Method           : GET
 :: URL              : http://10.48.179.191/FUZZ
 :: Wordlist         : FUZZ: /usr/share/seclists/Discovery/Web-Content/big.txt
 :: Follow redirects : false
 :: Calibration      : false
 :: Timeout          : 10
 :: Threads          : 40
 :: Matcher          : Response status: 200
________________________________________________

README.md               [Status: 200, Size: 9180, Words: 1164, Lines: 190, Duration: 51ms]
favicon.ico             [Status: 200, Size: 1406, Words: 5, Lines: 2, Duration: 69ms]
robots.txt              [Status: 200, Size: 26, Words: 3, Lines: 2, Duration: 64ms]
:: Progress: [20481/20481] :: Job [1/1] :: 638 req/sec :: Duration: [0:00:35] :: Errors: 0 ::

==============================================================================================================


2. **ffuf -u http://10.48.179.191/FUZZ -w /usr/share/seclists/Discovery/Web-Content/raft-medium-words-lowercase.txt -e .txt**

________________________________________________

 :: Method           : GET
 :: URL              : http://10.48.179.191/FUZZ
 :: Wordlist         : FUZZ: /usr/share/seclists/Discovery/Web-Content/raft-medium-words-lowercase.txt
 :: Extensions       : .txt 
 :: Follow redirects : false
 :: Calibration      : false
 :: Timeout          : 10
 :: Threads          : 40
 :: Matcher          : Response status: 200-299,301,302,307,401,403,405,500
________________________________________________

.php                    [Status: 403, Size: 284, Words: 21, Lines: 11, Duration: 40ms]
.html                   [Status: 403, Size: 285, Words: 21, Lines: 11, Duration: 41ms]
.html.txt               [Status: 403, Size: 289, Words: 21, Lines: 11, Duration: 36ms]
.htm                    [Status: 403, Size: 284, Words: 21, Lines: 11, Duration: 37ms]
config                  [Status: 301, Size: 314, Words: 20, Lines: 10, Duration: 47ms]
docs                    [Status: 301, Size: 312, Words: 20, Lines: 10, Duration: 53ms]
.htm.txt                [Status: 403, Size: 288, Words: 21, Lines: 11, Duration: 3268ms]
.                       [Status: 302, Size: 0, Words: 1, Lines: 1, Duration: 37ms]
external                [Status: 301, Size: 316, Words: 20, Lines: 10, Duration: 53ms]
.htaccess               [Status: 403, Size: 289, Words: 21, Lines: 11, Duration: 44ms]
.htaccess.txt           [Status: 403, Size: 293, Words: 21, Lines: 11, Duration: 53ms]
robots.txt              [Status: 200, Size: 26, Words: 3, Lines: 2, Duration: 45ms]

==============================================================================================================

3. **ffuf -u http://10.48.179.191/indexFUZZ -w /usr/share/seclists/Discovery/Web-Content/web-extensions.txt**          

________________________________________________

 :: Method           : GET
 :: URL              : http://10.48.179.191/indexFUZZ
 :: Wordlist         : FUZZ: /usr/share/seclists/Discovery/Web-Content/web-extensions.txt
 :: Follow redirects : false
 :: Calibration      : false
 :: Timeout          : 10
 :: Threads          : 40
 :: Matcher          : Response status: 200-299,301,302,307,401,403,405,500
________________________________________________

.phps                   [Status: 403, Size: 290, Words: 21, Lines: 11, Duration: 43ms]
.php                    [Status: 302, Size: 0, Words: 1, Lines: 1, Duration: 72ms]
:: Progress: [43/43] :: Job [1/1] :: 17 req/sec :: Duration: [0:00:02] :: Errors: 0 ::

==============================================================================================================


4. **ffuf -u http://10.49.173.75/FUZZ -w /usr/share/seclists/Discovery/Web-Content/raft-medium-directories-lowercase.txt**
________________________________________________

 :: Method           : GET
 :: URL              : http://10.49.173.75/FUZZ
 :: Wordlist         : FUZZ: /usr/share/seclists/Discovery/Web-Content/raft-medium-directories-lowercase.txt
 :: Follow redirects : false
 :: Calibration      : false
 :: Timeout          : 10
 :: Threads          : 40
 :: Matcher          : Response status: 200-299,301,302,307,401,403,405,500
________________________________________________

docs                    [Status: 301, Size: 310, Words: 20, Lines: 10, Duration: 79ms]
config                  [Status: 301, Size: 312, Words: 20, Lines: 10, Duration: 71ms]
external                [Status: 301, Size: 314, Words: 20, Lines: 10, Duration: 86ms]
server-status           [Status: 403, Size: 292, Words: 21, Lines: 11, Duration: 117ms]

==============================================================================================================


5. **ffuf -u http://10.49.173.75/FUZZ -w /usr/share/seclists/Discovery/Web-Content/raft-medium-files-lowercase.txt -fr '/\..*' -fc 403**

________________________________________________

 :: Method           : GET
 :: URL              : http://10.49.173.75/FUZZ
 :: Wordlist         : FUZZ: /usr/share/seclists/Discovery/Web-Content/raft-medium-files-lowercase.txt
 :: Follow redirects : false
 :: Calibration      : false
 :: Timeout          : 10
 :: Threads          : 40
 :: Matcher          : Response status: 200-299,301,302,307,401,403,405,500
 :: Filter           : Response status: 403
 :: Filter           : Regexp: /\..*
________________________________________________

login.php               [Status: 200, Size: 1523, Words: 89, Lines: 77, Duration: 45ms]
index.php               [Status: 302, Size: 0, Words: 1, Lines: 1, Duration: 38ms]
favicon.ico             [Status: 200, Size: 1406, Words: 5, Lines: 2, Duration: 50ms]
logout.php              [Status: 302, Size: 0, Words: 1, Lines: 1, Duration: 51ms]
robots.txt              [Status: 200, Size: 26, Words: 3, Lines: 2, Duration: 36ms]
phpinfo.php             [Status: 302, Size: 0, Words: 1, Lines: 1, Duration: 39ms]
.                       [Status: 302, Size: 0, Words: 1, Lines: 1, Duration: 45ms]
php.ini                 [Status: 200, Size: 148, Words: 17, Lines: 5, Duration: 38ms]
**about.php**               [Status: 200, **Size: 4840**, Words: 331, Lines: 109, Duration: 46ms]
setup.php               [Status: 200, Size: 4066, Words: 308, Lines: 123, Duration: 48ms]
security.php            [Status: 302, Size: 0, Words: 1, Lines: 1, Duration: 41ms]
:: Progress: [16244/16244] :: Job [1/1] :: 626 req/sec :: Duration: [0:00:28] :: Errors: 0 :

==============================================================================================================


6. **ffuf -u http://10.49.173.75/FUZZ -w /usr/share/seclists/Discovery/Web-Content/raft-medium-files-lowercase.txt -fr '/\..*'**

________________________________________________

 :: Method           : GET
 :: URL              : http://10.49.173.75/FUZZ
 :: Wordlist         : FUZZ: /usr/share/seclists/Discovery/Web-Content/raft-medium-files-lowercase.txt
 :: Follow redirects : false
 :: Calibration      : false
 :: Timeout          : 10
 :: Threads          : 40
 :: Matcher          : Response status: 200-299,301,302,307,401,403,405,500
 :: Filter           : Regexp: /\..*
________________________________________________

index.php               [Status: 302, Size: 0, Words: 1, Lines: 1, Duration: 50ms]
favicon.ico             [Status: 200, Size: 1406, Words: 5, Lines: 2, Duration: 46ms]
logout.php              [Status: 302, Size: 0, Words: 1, Lines: 1, Duration: 50ms]
robots.txt              [Status: 200, Size: 26, Words: 3, Lines: 2, Duration: 53ms]
phpinfo.php             [Status: 302, Size: 0, Words: 1, Lines: 1, Duration: 45ms]
.                       [Status: 302, Size: 0, Words: 1, Lines: 1, Duration: 135ms]
php.ini                 [Status: 200, Size: 148, Words: 17, Lines: 5, Duration: 81ms]
login.php               [Status: 200, Size: 1523, Words: 89, Lines: 77, Duration: 845ms]
about.php               [Status: 200, Size: 4840, Words: 331, Lines: 109, Duration: 76ms]
setup.php               [Status: 200, Size: 4066, Words: 308, Lines: 123, Duration: 46ms]
security.php            [Status: 302, Size: 0, Words: 1, Lines: 1, Duration: 98ms]
**wp-forum.phps**           [Status: 403, Size: 292, Words: 21, Lines: 11, Duration: 67ms]
-- Extra FILE APPEAR IN '-fr' which usually not appears in '-fc'

==============================================================================================================

7. **ffuf -u 'http://10.48.155.74/sqli-labs/Less-1/?FUZZ=1' -c -w /usr/share/seclists/Discovery/Web-Content/burp-parameter-names.txt -fw 39**

- filter the results which contains exactly 39 words because this is normal boring irrelavent keyword.
- Run FFUF normally
        ↓  
Look at Size / Words / Lines
        ↓
Find the common response
        ↓
Filter that common response
        ↓
Investigate the unusual responses

________________________________________________

 :: Method           : GET
 :: URL              : http://10.48.155.74/sqli-labs/Less-1/?FUZZ=1
 :: Wordlist         : FUZZ: /usr/share/seclists/Discovery/Web-Content/burp-parameter-names.txt
 :: Follow redirects : false
 :: Calibration      : false
 :: Timeout          : 10
 :: Threads          : 40
 :: Matcher          : Response status: 200-299,301,302,307,401,403,405,500
 :: Filter           : Response words: 39
________________________________________________

id                      [Status: 200, Size: 721, Words: 37, Lines: 29, Duration: 169ms]
:: Progress: [6453/6453] :: Job [1/1] :: 607 req/sec :: Duration: [0:00:12] :: Errors: 0 ::

==============================================================================================================

8. **for i in {0..255}; do echo $i; done | ffuf -u 'http://10.48.155.74/sqli-labs/Less-1/?id=FUZZ' -c -w - -fw 33**

________________________________________________

 :: Method           : GET
 :: URL              : http://10.48.155.74/sqli-labs/Less-1/?id=FUZZ
 :: Wordlist         : FUZZ: -
 :: Follow redirects : false
 :: Calibration      : false
 :: Timeout          : 10
 :: Threads          : 40
 :: Matcher          : Response status: 200-299,301,302,307,401,403,405,500
 :: Filter           : Response words: 33
________________________________________________

4                       [Status: 200, Size: 725, Words: 37, Lines: 29, Duration: 46ms]
1                       [Status: 200, Size: 721, Words: 37, Lines: 29, Duration: 47ms]
11                      [Status: 200, Size: 725, Words: 37, Lines: 29, Duration: 45ms]
6                       [Status: 200, Size: 728, Words: 37, Lines: 29, Duration: 45ms]
3                       [Status: 200, Size: 726, Words: 37, Lines: 29, Duration: 450ms]
**14**                      [Status: 200, Size: 725, Words: 37, Lines: 29, Duration: 3320ms]
-HIGHEST VALID ID-
9                       [Status: 200, Size: 725, Words: 37, Lines: 29, Duration: 3320ms]
2                       [Status: 200, Size: 731, Words: 37, Lines: 29, Duration: 3320ms]
10                      [Status: 200, Size: 725, Words: 37, Lines: 29, Duration: 4056ms]
12                      [Status: 200, Size: 725, Words: 37, Lines: 29, Duration: 4058ms]
7                       [Status: 200, Size: 725, Words: 37, Lines: 29, Duration: 4064ms]
5                       [Status: 200, Size: 728, Words: 37, Lines: 29, Duration: 4068ms]
8                       [Status: 200, Size: 723, Words: 37, Lines: 29, Duration: 4069ms]
:: Progress: [256/256] :: Job [1/1] :: 52 req/sec :: Duration: [0:00:04] :: Errors: 0 ::

==============================================================================================================

9. **ffuf -u http://10.48.155.74/sqli-labs/Less-11/ -c -w /usr/share/seclists/Passwords/Leaked-Databases/hak5.txt -X POST -d 'uname=Dummy&passwd=FUZZ&submit=Submit' -fs 1435 -H 'Content-Type: application/x-www-form-urlencoded'**

_________________________

 :: Method           : POST
 :: URL              : http://10.48.155.74/sqli-labs/Less-11/
 :: Wordlist         : FUZZ: /usr/share/seclists/Passwords/Leaked-Databases/hak5.txt
 :: Header           : Content-Type: application/x-www-form-urlencoded
 :: Data             : uname=Dummy&passwd=FUZZ&submit=Submit
 :: Follow redirects : false
 :: Calibration      : false
 :: Timeout          : 10
 :: Threads          : 40
 :: Matcher          : Response status: 200-299,301,302,307,401,403,405,500
 :: Filter           : Response size: 1435
________________________________________________

p@ssword                [Status: 200, Size: 1526, Words: 100, Lines: 50, Duration: 44ms]
:: Progress: [2351/2351] :: Job [1/1] :: 353 req/sec :: Duration: [0:00:06] :: Errors: 0 ::


==============================================================================================================

10. **ncat -l 8080 --proxy-type http**
**ffuf -u http://10.49.145.57/FUZZ -c -w /usr/share/seclists/Discovery/Web-Content/common.txt -x http://127.0.0.1:8080**

________________________________________________

 :: Method           : GET
 :: URL              : http://10.49.145.57/FUZZ
 :: Wordlist         : FUZZ: /usr/share/seclists/Discovery/Web-Content/common.txt
 :: Follow redirects : false
 :: Calibration      : false
 :: Proxy            : http://127.0.0.1:8080
 :: Timeout          : 10
 :: Threads          : 40
 :: Matcher          : Response status: 200-299,301,302,307,401,403,405,500
________________________________________________

.htpasswd               [Status: 403, Size: 296, Words: 22, Lines: 12, Duration: 121ms]
.htaccess               [Status: 403, Size: 296, Words: 22, Lines: 12, Duration: 215ms]
.hta                    [Status: 403, Size: 291, Words: 22, Lines: 12, Duration: 156ms]
server-status           [Status: 403, Size: 300, Words: 22, Lines: 12, Duration: 93ms]
:: Progress: [4750/4750] :: Job [1/1] :: 110 req/sec :: Duration: [0:00:32] :: Errors: 0 ::

==============================================================================================================





