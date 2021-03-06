# eForth for STM32F407 Discovery board

## local studies by wa1tnr
`Target board:` **Adafruit STM32F405 Express**

`Target board:` **STM32F407 Discovery**

### current: Fri Sep  4 16:19:40 UTC 2020

#### NEWS

##### Applications repository begun

This (new) repository is meant to put some of the developed
forth source code onto github.

Included are routines to setup a second USART, in forth,
and also to talk to the Lumex display (discussed elsewhere).

##### STM32F407 Discovery - primary target

The STM32F407 Discovery was received in the post, from
DigiKey, earlier in the year, and became the primary
target for the program, as a result (needed to have
the extra GPIO pins not available on the Adafruit
target, which is otherwise suitable).

##### Lumex 96x8 RGB matrix, 3mm pitch, supported.

The Lumex display uses Hayes style 'AT' commands.

The trick to messaging to the display is to do so
continuously; if there's much of a delay, then the
display will not accumulate the message - it will
start over again at the left margin, after blanking
the entire display.

The Lumex display support was written entirely in Forth. ;)

Including the setup for the second USART pin pair.

Code that exists is either in a branch (not master)
or hasn't even been uploaded to github.  Sorry. ;)

That will change at some point; too much work was
done without public commits.  Hard to separate out
private code from public.

### older: Sat Jun 20 13:09:01 UTC 2020

Current effort:

get a second USART working, on PC6/TX, PC7/RX pair.

Intent is to send messages to a Lumex 96x8 display,
while retaining full dialogue with the target, in
the eForth environment.

### older: Tue Dec 17 22:00:36 UTC 2019

from: doc/notes.txt

Tue Dec 17 22:55:21 UTC 2019

Dr. C.H. Ting's eForth for the STM32F407 Discovery board:

    http://forth.org/OffeteStore/OffeteStore.html

    STM32 eForth - 2014

        http://forth.org/OffeteStore/2165_stm32eForth720.zip


Target board:  Adafruit STM32F405 Express

  http://adafru.it/4382

Dr. Ting's eForth runs (unmodified) on the Adafruit board.
GPIO support is on four unavailable pins, however.

TX/RX (for USART1) is brought out on (STM32F405 Express) SCL/SDA.


rename repository:

  eforth-stm4x-a > eforth-stm32f4x-a


Tue Dec 17 22:03:02 UTC 2019

```bash
** initial-dev
  master
```

```bash
 $ git checkout -b initial-dev
```
Switched to a new branch 'initial-dev'
```bash
 $ mkdir doc
 $ cd doc
 $ rvim -n notes.txt
 $ git branch >> notes.txt
```

 and the rest of what's seen here (now).

**FOOTNOTES**

  **04 SEP 2020**

    No real effort was made to be cohesive, today.

    This 'apps' repository is meant to somewhat deviate the
    previous course held (long development, essentially
    in private, where it does not need to be).

    So, aspirationally, effort is now made to present what's
    learned, where the public can benefit from it.

    Again, not particularly cohesive .. just a beginning.


**REFERENCES**

   **Markdown**:

   [https://guides.github.com/features/mastering-markdown/]

END.
