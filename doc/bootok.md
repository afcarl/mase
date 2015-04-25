
[Home](https://github.com/txt/mase/blob/master/README.md) | [Contents](https://github.com/txt/mase/blob/master/TOC.md) | [About](https://github.com/txt/mase/blob/master/ABOUT.md) | [Syllabus](https://github.com/txt/mase/blob/master/SYLLABUS.md) | [Code](https://github.com/txt/mase/tree/master/src) [Contact](http://menzies.us)   
[<img width=900 src="https://raw.githubusercontent.com/txt/mase/master/img/banner.png">](https://github.com/txt/mase/blob/master/README.md)



# Boot test routines.

````python

from boot import * # get the test engine

@ok # run+test something at load time
def noop(): return True # never fails

@ok # ditto
def oops(): 1/0  # always fails

@ok # eg3: test the test engine
def unittestok():
  ok(oops,       # "ok" accepts multiple arguments
    noop,        # can be named functions
    lambda: 1+1, # or anonymous functions
    lambda: 1/0
    )
  ok(oops)       # ok can also run with 1 test
  ok(oops,noop)
  # note that, when runm we never see 'unitest fail'
  assert unittest.tries == 10, 'unit test fail'
  assert unittest.fails == 5,  'unit test fail'

print("\n"+"EXPECT...... # TRIES= 10 FAIL= 5 %PASS = 67%")
print("GOT.........",unittest.score())
````

__________


![lic](img/license.png)

Copyright © 2015 [Tim Menzies](http://menzies.us), email: <tim.menzies@gmail.com>.

This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to <http://unlicense.org/>

