# Spec Test Library

A Spec test library dedicated to the Thicket language.

## Description / API

```
def simpleAssertions : TestLogger -> unit = logger -> {
    description logger "Simple Assertion tests"
        it "expect true toBe true" {
            expect true toBe true
        }
        it "expect true not toBe false" {
            expect true not toBe false
        }
        it "expect false toBe false" {
            expect false toBe false
        }
        it "expect 1 not toBe 2" {
           expect 1 not toBe 2
        }
        it "expect 1 not toBe (-1)" {
           expect 1 not toBe (-1)
        }
        it "expect 1 toBe 1" {
            expect 1 toBe 1
        }
        it "expect 1 toBeIn List[1]" {
            expect 1 toBeIn $ List[1]
        }
        it "expect 1 toBeAKey Hashmap[1=>'a']" {
            expect 1 toBeAKey $ Hashmap[1=>"a"]
        }
        it "expect 1 not toBeAKey Hashmap[2=>'a']" {
            expect 1 not toBeAKey $ Hashmap[2=>"a"]
        }
        it "expect 'a' toBeAValue Hashmap[1=>'a']" {
            expect "a" toBeAValue $ Hashmap[1=>"a"]
        }
        it "expect 'b' not toBeAValue Hashmap[2=>'a']" {
            expect "b" not toBeAValue $ Hashmap[2=>"a"]
        }  
    done 
}
```

## Project construction

The following command  build, test and intall the package in the
user local repository i.e. `~/.thicket/site` directory on unix
based system.

```sh 
> ls
LICENSE         bin         package-test.pkt    src
README.md       obj         package.pkt

> $THICKET_HOME/bin/thicket project install
...
```

## License

Copyright (C)2015 D. Plaindoux.

This program is  free software; you can redistribute  it and/or modify
it  under the  terms  of  the GNU  Lesser  General  Public License  as
published by  the Free Software  Foundation; either version 2,  or (at
your option) any later version.

This program  is distributed in the  hope that it will  be useful, but
WITHOUT   ANY  WARRANTY;   without  even   the  implied   warranty  of
MERCHANTABILITY  or FITNESS  FOR  A PARTICULAR  PURPOSE.  See the  GNU
Lesser General Public License for more details.

You  should have  received a  copy of  the GNU  Lesser General  Public
License along with  this program; see the file COPYING.  If not, write
to the  Free Software Foundation,  675 Mass Ave, Cambridge,  MA 02139,
USA.

