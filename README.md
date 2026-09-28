# homing-pigeon
A tool that takes any misshapen address and reformats it to USPS delivery address standards. The name is inspired by homing pigeons who always find their way to the right address.

# Homing Pigeon

A tool that takes any misshapen address and reformats it to [USPS delivery address standards](https://pe.usps.com/businessmail101?ViewName=DeliveryAddress) (all caps, no punctuation, standard abbreviations, correct spacing). If something looks missing — a ZIP code, an apartment number — it drafts a follow-up text you can send back to ask for it.  My most common use case for this tool is reformatting addresses which my friends send me over text, since they often span different syntatic styles. 

It's a single HTML file. No build step, no backend, no dependencies.

The name is inspired by homing pigeons, domestic pigeons who are used to send mail because find their way to the right address.

## Using it

1. Paste the address text into the box and click **Read address**.
2. It'll guess at name / company / street / unit / city / state / ZIP and drop them into editable fields — check them, since parsing free-form text is never perfect (a name with a street-suffix-sounding word in it, for instance, can trip it up).
3. Click **Format address** to get the USPS-formatted block, with a note if anything's missing.
4. Copy the formatted address, or copy the drafted follow-up message to send back to your friend.


## Colors

The palette is the seven-color set that USPS and the Pantone Color Institute created for the Postal Service's 250th anniversary:

| Color | Hex | Used for |
| --- | --- | --- |
| USPS Blue | `#1C4883` | Page background |
| USPS Parchment White | `#FFFDEE` | Address and message cards |
| USPS Airmail Red | `#DB3B39` | Primary buttons |
| USPS Carrier Red | `#6E131A` | Button hover, warnings, links on cards |
| USPS Mr. ZIP Orange | `#E16E39` | "Things to check" marker |
| USPS Gold Seal | `#C58C2F` | "Looks complete" marker |
| USPS Pony Express | `#5F443D` | "Looks complete" text |

Sources: [USPS Link, "These colors paint the history of USPS"](https://news.usps.com/2025/08/26/these-colors-paint-the-history-of-usps/) and [Pantone x USPS](https://www.pantone.com/usps250). The hex values were sampled from the swatches on the Pantone page, so treat them as close matches rather than official specifications. A few shades of USPS Blue (panels, inputs, borders) are derived from it and are defined separately in the CSS.

USPS's article says these colors were created for marketing purposes to mark the anniversary. This is an independent project and isn't affiliated with or endorsed by USPS or Pantone.

This tool formats addresses; it does not validate that they're real, deliverable, or CASS-certified — USPS's own [ZIP Code Lookup](https://tools.usps.com/zip-code-lookup.htm) is the source of truth for that.

Built with help from Claude Code (Anthropic).

