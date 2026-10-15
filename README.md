# The Individual Use Licence

Version 1.0.0. Drafted 2026-10-15. **Not yet applied to any repository.**

Free for people. Free for small outfits. Paid for everyone else. Not open source,
and it says so.

The licence text is [`LICENSE`](./LICENSE).

## Status

Nothing uses this licence yet. It is a draft for review, not a finished instrument.
Do not attach it to a repository until at least the contact address below is filled
in.

## Before you use it: two required edits

`LICENSE` contains two placeholders, and both matter. `grep -n '<<' LICENSE`
finds them.

**`<<LICENCE CONTACT>>`**, in **How to Request a Paid Licence**. This section is
load-bearing: it is one half of the anti-hostage bargain (see below), and a
licence with no way to request terms is a licence nobody can buy.

**`<<LICENCE URL>>`**, in the header. The **Notices** section requires anyone
passing the software on to give recipients these terms *or the URL for them*, so
this has to be a real, permanent location — the repository holding the canonical
text. Until it exists, that half of the Notices requirement points at nothing.

## The tiers

| Tier | Who | Cost |
| --- | --- | --- |
| **Individual Use** | Any natural person, acting for themselves alone. Any purpose, including commercial and self-employed work. | Free |
| **Small Organisation** | Fewer than **8** people, under **$400,000** revenue, under **$400,000** investment over five years | Free |
| **Paid Use** | Everyone else | Paid licence, terms to be set |

### Where the numbers came from

Adapted from a predecessor licence whose free tier was **20 people / $1,000,000 /
$1,000,000**. The user asked for the headcount to drop to 8 and the money thresholds
to drop "accordingly", so both money figures were scaled by the same ratio as the
headcount:

```
8 / 20 = 0.4        1,000,000 x 0.4 = 400,000
```

Hence **8 people / $400,000 / $400,000**. This is a proportional scaling, not a
researched figure. The revenue threshold is now low enough that it will capture
genuine micro-businesses, which is presumably the intent — but if it turns out to
catch more than intended, raise the revenue figure rather than the headcount, since
headcount is the harder one to game.

All figures are USD as of 2019 and adjust for inflation by US BLS CPI-U, carried
over from the predecessor text.

## The three things this licence does that older ones do not

**1. It charges large organisations rather than asking them nicely.** The free tier
is bounded by headcount, revenue *and* investment. Investment is counted over five
years and includes predecessor companies, so a well-funded startup cannot pass
itself off as small.

**2. It cannot be held hostage.** The Paid Use section grants a large organisation
the right to use the software **indefinitely and free** if the licensor does not
offer fair, reasonable and non-discriminatory terms within **32 days** of a written
request. This looks like a concession and is actually the enforcement mechanism: it
is what stops a corporate legal team from simply banning the dependency, because
they know they cannot be extorted. It also means the licence stops working if the
licensor dies, vanishes or ignores their email — which is the honest outcome, since
an unreachable licensor is not running a licensing business.

There is also a **128-day grace period** after an organisation stops qualifying, so
growth is not an ambush.

**3. It takes a position on AI.** Two sections, and they are the novel part:

- **Machine-Written Software** — the licensor discloses up front that substantial
  portions were produced by machine, claims no copyright where there is no human
  author, and requires that anyone passing the software on does not misrepresent
  machine-written portions as human work or attach copyright notices to output with
  no human author.
- **Training and Models** — training a model on the software *is* use of the
  software; the resulting model is a derivative and must be licensed under these
  same terms; and use of such a model by a large organisation is itself Paid Use.

The mechanism is deliberate. Rather than inventing a novel "no AI training"
prohibition — which is untested and easy to argue around — the training clause
reuses the existing size thresholds. A hobbyist trains freely. An AI lab needs a
paid licence, and a model trained on this code inherits the same rule: free for
people, paid for companies. That is the reciprocity working as intended.

## Provenance

Adapted from the **Big Time Public License 2.0.2**
(<https://bigtimelicense.com/versions/2.0.2>), whose own meta-licence grants
everyone permission to do everything with its text on one condition: that a changed
version **removes all mention of "Big Time"**.

That condition is honoured — the word appears nowhere in `LICENSE`. It is named
here instead, because this file is documentation rather than the licence itself, and
because provenance that has to be hidden is provenance worth writing down.

**PolyForm was rejected as a base.** Its licence suite is a good structural model
and was studied for this draft, but the repository holding its source text declares
no licence at all (`polyformproject/polyform-licenses` reports `license: none`), so
its text is not ours to adapt. Its ideas are, and the tier structure here owes
something to it.

## Naming

**The Individual Use Licence**, acronym **IUL**, identifier `IUL-1.0.0`. In
prose, *the IUL* — as short as *the GPL*.

*Use* names the licence's headline grant: permission to use the software is free
for individuals and paid for everyone else. PolyForm works the same way — the
*PolyForm Small Business License* contains a `Small Business` section — so a
licence carrying both a name and an `## Individual Use` section is a familiar
shape rather than a collision.

### Why not a `-PL` acronym

`IPL` was the obvious first choice and is not available. SPDX assigns `IPL-1.0`
to the *IBM Public License v1.0*, so package metadata reading `IPL` is read as
IBM's licence — a different and much older thing.

The whole `-PL` namespace turns out to be exhausted. Every natural three-letter
combination is taken: `APL` (Adaptive), `IPL` (IBM), `LPL` (Lucent), `MPL`
(Mozilla), `NPL` (Netscape), `OPL` (Open Public, and the UK's Open Parliament
Licence), `PPL` (Peer Production) and `SPL` (Sun). No reordering of *Individual
… Public Licence* yields a free one, which is how `Public` came to be dropped.

That left *The Individual Licence*, whose acronyms were `IL` and `TIL` — both
weak, and `TIL` is spoken for as "today I learned". Swapping *Licence* for *Use
Licence* produced **IUL**, verified unclaimed:

```
Identifier: IUL-1.0.0
```

`Individual` is unclaimed as a namespace too: no SPDX identifier begins with
`Ind`, and no licence in the register uses the words *Individual*, *Person*,
*Human*, *Solo* or *Indie*.

**IFL** (*Individual Free Licence*) and **ICL** (*Individual Commons Licence*)
are also free, but should be avoided: *Free* and *Commons* both read as
open-source-adjacent, which is the one thing this licence emphatically is not.

### Why not "Post-Open"

*Individual Post-Open Licence* would give the free acronym **IPOL** — verified
unclaimed in SPDX, and no licence in the register mentions post-open at all. It
is still the wrong name, for one reason: **Post-Open is not a generic term, it is
the name of an active project.**

Bruce Perens' [postopen.org](https://postopen.org/) is a specific thing — a
licence draft, a Post Open Administration seeking 501(c)4 status, an Operating
Agreement, developer IDs, cryptographic devices and a code of conduct. Every
search for the phrase returns that project. Naming this licence after it would
imply an affiliation that does not exist, and would misdescribe the text: his
Post-Open is an *institution*, while this licence deliberately has none — no
membership, no administrator, no agreement to sign. That institutional machinery
is precisely what was rejected when Post-Open was considered in the first place.

The paradigm break belongs in the Preamble, where it already is — *"It is not
open source, and you must not call it open source."* The GPL did not call itself
post-BSD.

### What changed, and why

This was briefly *The Individual **Public** Licence*. *Public* was dropped. The
tradition behind it is real — GNU GPL, Mozilla Public License, LaTeX Project
Public License, the WTFPL's own *Do What The F\*ck You Want To **Public**
License*, and the EUPL for the GB spelling — and it usefully signalled that the
text is a standard form anyone may adopt, which is what the Meta Licence grants.
But it carried a misreading risk: a procurement reader skimming the name could
take *Public* to mean the software is in the public domain, which is close to the
opposite of the point. The Preamble disposed of that in a paragraph; dropping the
word was simpler than defending it.

What survived all of it: **The Individual Use Licence**, **IUL**, `IUL-1.0.0`.

## House style

- **GB English throughout.** Noun is *licence*, verb is *license*; `licensor`,
  `licensee` and `licensed` keep the `s` in both variants. There is no "licencor".
- `-ise` endings: *organisation*, *reorganised*, *recognisably*.
- *program* for software, *enquiries* for questions asked, *spun out* for a
  corporate spin-out.
- The file is named `LICENSE` (US spelling) while the title inside is *Licence*.
  This is deliberate. GitHub detects either — its detector matches
  `/(un)?licen[sc]e/i` — but third-party compliance scanners are more consistently
  familiar with `LICENSE`, and being read correctly by those scanners is the entire
  point of this licence. Rename to `LICENCE` if consistency matters more; detection
  will still work.

## Known limitations

**The teeth are on human-written code.** This is a copyright licence. Where machine
output has no human author there may be no copyright to license, so the size
thresholds have nothing to bite on. The Acceptance section ("strict obligations and
conditions") creates a contract hook that partly covers the gap, but over the
machine-written portions of a repository this licence is closer to a statement of
position than an enforceable mechanism. That is not fixable by drafting; it is the
state of copyright law.

**You will not be doing the enforcing.** A solo developer does not litigate against
a corporation. What actually happens is that a compliance scanner flags the
repository in a customer's build, their legal team reads these terms, and either
pays or drops the dependency. That is the real collection mechanism, and it is why
the file naming, the plain structure and the 32-day anti-hostage clause matter more
than rhetorical force.

**A bespoke licence scans as "Unknown".** No SPDX identifier, so scanners treat it
as maximum risk. Some organisations will avoid the software rather than engage. This
is the price of a licence that says something no existing licence says.

## Not decided yet

- The contact address (required — see above).
- Whether paid terms will be advertised with a public price, which matters because
  the FRAND section defines fairness partly by reference to advertised terms.
- What the paid licence actually costs, or whether it is negotiated case by case.
- Which repositories this will be applied to. Deliberately **not** the `bqv/bqv`
  profile repository, which carries no code to license.

## Related

- Design brief and the research behind it: `~/ref/POST-OPEN-LICENSE.md`
- Standing-rule change this relates to: the `AGENTS.md` rule preferring MPL-2.0 for
  new repositories is **kept**, and will be followed immediately by a line
  superseding it with this licence for the cases where it applies. Not yet edited,
  pending this text existing — which it now does.
