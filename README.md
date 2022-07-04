# PHP to PHP 3 Converter
Convert PHP code back to working PHP 3 code!

## Disclaimer
- Not all PHP 4/5/6/7/8 functions and language constructs are supported
- Not all functions or constructs support all parameters as in their original implentation
- Class features are not a main part of this project, so you usually won't be able to use PHP 4+ object-oriented programming
- You may need to install libraries as old PHP modules do not work anymore together with new libraries

## How it technically works
1. The program screens the script for functions, checks if they work in PHP 3, depending on the function using a given list or by trying
2. Errors are being printed if some function can't be replaces
3. For some function, it is enough to add define them at top of the script
2. Warinings are being printed if some function can't be replaces well, f.e. if the polyfill does not support all requested features
4. Other functions are being analyzed and rewritten as a new block of code
5. It now scans for language constructs and rewrites the affected code blocks
6. Depending on the configuration, a temporary or permanent file is being generated, executed and removed

## Download PHP 3

### For Linux / macOS / etc.
Download Link: http://museum.php.net/php3/php-3.0.18.tar.gz (PHP 3.0.18)
```
cd Downloads && tar -zxvf php-3.0.18.tar.gz && cd php-3.0.18
./buildconf && ./configure && make -j $(nproc)
./php -v
```
Succesful compilation tested on Ubuntu and Debian (Kali) in 2022. No root access required.

### For Windows
Download Link: http://museum.php.net/win32/php-3.0.17-win32.zip (PHP 3.0.17)

## Features

As the script is written in PHP 3, you only need PHP 3 for it to work.

### Language Constructs
- foreach (PHP 4+)
- require_once (PHP 4+)
- include_once (PHP 4+)
- closures (PHP 5.3+)
- short array definition (PHP 5.4+)

### Functions
Most are PHP 4+, some are PHP 7+ and PHP 8+
- array_braces
- array_diff
- array_key_exists
- array_keys
- array_map
- array_merge
- array_pop
- array_push
- array_reverse
- array_search
- array_shift
- array_slice
- array_unique
- array_unshift
- array_values
- date_default_timezone_set
- declare
- file_get_contents
- file_put_contents
- func_get_args
- get_defined_vars
- in_array
- ini_set
- is_bool
- is_callable
- is_null
- is_numeric
- ob_end_clean
- ob_get_contents
- ob_start
- php_sapi_name
- require_once
- shell_exec
- str_contains
- str_ends_with
- str_repeat
- str_starts_with


## Supported by default in PHP 3

This list is not complete and only refers to most used features.

### Language Constructs and Reserved Keywords
and, array, break, case, catch, class, continue, die, do, echo, else, elseif, empty, endif, endswitch, endwhile, exit, for, function, global, if, include, isset, list, new, or, print, print_r, require, return, switch, unserialize, unset, while

### Functions (extract)
base64_encode, basename, call_user_func, ceil, chr, count, current, date, defined, dirname, end, error_reporting, eval, explode, extension_loaded, fclose, file_exists, floor, fopen, function_exists, fwrite, gettype, header, htmlspecialchars, implode, intval, is_array, is_dir, is_file, is_int, is_string, krsort, ksort, ltrim, min, max, md5, microtime, mkdir, next, ord, parse_url, phpversion, preg_match, preg_match_all, preg_replace, preg_split, reset, rtrim, serialize, sprintf, strlen, strpos, strtolower, strtotime, strtoupper, strtr, substr, time, trim, ucfirst, uniqid, urlencode, var_dump
