# Colmak keyboards

To make the transition to Colemak easier there are 5 layouts used commonly - there is a whole discussion here about the many layouts and variants [here](https://forum.colemak.com/topic/1858-learn-colemak-in-steps-with-the-tarmak-layouts/).

## Linux configuration

Add each layout configuration section to file `/usr/share/X11/xkb/symbols`, and make sure you declare each layout in file `/usr/share/X11/xkb/rules/evdev.xml`: in the appropriate language.

### Tarmak 5 (Colemak)
```
//
// Portuguese Tarmak 5th level.
//     This is a Tarmak-based layout, designed for the Portuguese language and customized
//     for portuguese keyboard layouts.
//
partial alphanumeric_keys
xkb_symbols "pt-tarmak5" {
	include "latin(type4)"
    name[Group1]="Portuguese (Tarmak 5)";

    key <TLDE> { [     backslash,             bar,        notsign,          notsign ] };
    key <AE03> { [             3,      numbersign,       sterling,         sterling ] };
    key <AE04> { [             4,          dollar,        section,           dollar ] };
    key <AE11> { [    apostrophe,        question,      backslash,     questiondown ] };
    key <AE12> { [ guillemotleft,  guillemotright,   dead_cedilla,      dead_ogonek ] };

    key <AD01>  { [         q,          Q,           at,  Greek_OMEGA ] };
    key <AD02>  { [         w,          W,      lstroke,      Lstroke ] };
    key <AD03>  { [         f,          F,            f,            F ] };
    key <AD04>  { [         p,          P,    paragraph,   registered ] };
    key <AD05>  { [         g,          G,       tslash,       Tslash ] };
    key <AD06>  { [         j,          J,    leftarrow,          yen ] };
    key <AD07>  { [         l,          L,    downarrow,      uparrow ] };
    key <AD08>  { [         u,          U,   rightarrow,     idotless ] };
    key <AD09>  { [         y,          Y,       oslash,     Ooblique ] };
    key <AD10>  { [         ccedilla,   Ccedilla,   thorn,        THORN ]   };

    key <AD11> { [          plus,        asterisk, dead_diaeresis,   dead_abovering ] };
    key <AD12> { [    dead_acute,      dead_grave,     dead_tilde,      dead_macron ] };
    key <BKSL> { [    dead_tilde, dead_circumflex,     dead_grave,       dead_breve ] };

    key <AC01>  { [         a,          A,           ae,           AE ] };
    key <AC02>  { [         r,          R,       ssharp,      section ] };
    key <AC03>  { [         s,          S,          eth,          ETH ] };
    key <AC04>  { [         t,          T,      dstroke,  ordfeminine ] };
    key <AC05>  { [         d,          D,          eng,          ENG ] };
    key <AC06>  { [         h,          H,      hstroke,      Hstroke ] };
    key <AC07>  { [         n,          N,    dead_hook,    dead_horn ] };
    key <AC08>  { [         e,          E,          kra,    ampersand ] };
    key <AC09>  { [         i,          I,      lstroke,      Lstroke ] };
    key <AC10>  { [         o,          O,      dead_acute, dead_doubleacute ]  };
    key <AC11> { [     masculine,     ordfeminine,dead_circumflex,       dead_caron ] };

    key <AB01>  { [         z,          Z, guillemotleft,        less ] };
    key <AB02>  { [         x,          X, guillemotright,    greater ] };
    key <AB03>  { [         c,          C,         cent,    copyright ] };
    key <AB04>  { [         v,          V, leftdoublequotemark, leftsinglequotemark ]   };
    key <AB05>  { [         b,          B, rightdoublequotemark, rightsinglequotemark ] };
    key <AB06>  { [         k,          K,            k,            K ] };
    key <AB07>  { [         m,          M,           mu,    masculine ] };

    key <LSGT> { [          less,         greater,      backslash,        backslash ] };

    include "level3(ralt_switch)"
};
```

## Windows installers
Find the windows installers in the `windows` directory.

## MacOS installer
Find the mac OS installers in the `mac` directory (created with [Ukelele](https://software.sil.org/ukelele/)).

---
#### Sources
- https://help.ubuntu.com/community/Custom%20keyboard%20layout%20definitions
- https://forum.colemak.com/topic/1858-learn-colemak-in-steps-with-the-tarmak-layouts/