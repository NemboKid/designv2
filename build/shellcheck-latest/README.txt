This is a precompiled ShellCheck binary.
      https://www.shellcheck.net/

ShellCheck is a static analysis tool for shell scripts.
It's licensed under the GNU General Public License v3.0.
Information and source code is available on the website.

This binary was compiled on Tue Nov 19 01:23:44 UTC 2019.



      ====== Latest commits ======

commit 5c7d8129ad3af8b99902dd656a0ffef3be1141d5
Author: Vidar Holen <spam@vidarholen.net>
Date:   Mon Nov 18 17:12:25 2019 -0800

    Try to search for binary on macOS/Cabal3

commit e075cde35792523140aa0506abc0423758151944
Author: Vidar Holen <spam@vidarholen.net>
Date:   Sat Nov 16 11:46:58 2019 -0800

    Revert docker image to 18.04 since ld fails on later versions

commit 9f578f41a1259b67f45976fe4eb61366239661b0
Author: Vidar Holen <spam@vidarholen.net>
Date:   Sat Nov 16 11:16:15 2019 -0800

    Explicitly add 'mappend' for old GHC versions
