# Panchang data — compute it, don't copy it

Tithi dates, nakshatras, sunrise/sunset times, and festival dates are
**facts**. Facts are not copyrightable in the US. What *is* copyrightable is
another site's text, layout, and presentation — so never scrape
DrikPanchang-style sites. Compute the values yourself and present them in
your own design.

## How to compute

1. **Ephemeris**: use JPL Development Ephemeris data (DE440/441) — produced
   by the US government, public domain. Gives precise sun/moon longitudes.
2. **Algorithms**: tithi = 12° of lunar elongation; nakshatra = 13°20'
   segments; standard sunrise equations. These are textbook astronomy, not
   anyone's property.
3. **Libraries**: several open-source panchang libraries exist (Python and
   JS). **Verify the library's license for commercial use before depending
   on one** — e.g. Swiss Ephemeris-based packages carry license restrictions.
   When in doubt, implement from JPL data + published algorithms.

## Disclose your method

Panchang values legitimately differ by tradition and parameter:

- **Ayanamsa**: Lahiri (most common in India) vs Raman vs Krishnamurti.
- **Month reckoning**: amanta (ends with new moon) vs purnimanta (ends with
  full moon) — festival dates can shift between regions because of this.
- **Sunrise definition**: center vs upper limb; elevation corrections.

State on the site: *"Computed using Lahiri ayanamsa; regional variations
exist."* This single line defuses most "your Diwali date is wrong" disputes —
the date usually isn't wrong, the *method* differs, and saying so up front
turns a controversy into a footnote.
