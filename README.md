# DFIR Toolkit

A single-page, searchable index of digital forensics and incident response tooling,
organised into categories by the kind of work they serve, plus a curated OPML of DFIR
and threat-intel feeds. The live page carries the current counts.

**Live:** https://dfir-toolkit.github.io/

## What it is

Each entry carries a name, URL, description, cost model (open source / free / commercial),
the platforms whose artifacts it examines, the platforms it runs on, an entry type
(tool, reference, blog, intel or training), and an interface (command line / GUI / browser).

## Structure

Categories are grouped into eight areas by the kind of work they serve:

| Area | Covers |
| --- | --- |
| Collect | Acquisition & imaging, memory acquisition, live response |
| Examine | Per-platform: Windows, macOS, Linux, iOS, Android, mobile suites, cloud, network |
| Analyse | Memory, timelines, logs, malware, reverse engineering, detection rules |
| Recover & decrypt | Carving, password recovery, ciphers, steganography |
| Threats & intel | Threat intel, OSINT, reputation lookups, ICS and embedded |
| Report & reference | Reporting, artifact references, standards, awesome lists |
| Learn | Training, CTFs, blogs, podcasts, test images and datasets |
| Environment | Distros and VMs, workstation and general tooling |

A tool has exactly one home category. Tools with genuine dual use are cross-listed
into the other categories where an investigator would look for them, marked on the
card. Cross-listings never inflate the total — the count is of tools, not listings.

## Search

Searches match names, descriptions, categories, platform tags and a capability index
that maps generalist tools to artifacts their own descriptions never name, so a search
for `prefetch` surfaces suites that parse it without saying so.

Searching a file extension or filename works directly — `.evtx`, `$MFT`, `knowledgeC.db`,
`.apk`, `.plist`, `.tracev3` — because an examiner usually arrives holding a file rather
than a category. Extensions are matched on word boundaries, so `.tar` does not drag in
every tool whose description mentions "startup".

Query syntax: spaces mean AND, a comma or `OR` separates alternatives, `"quoted text"`
matches as a phrase, and a leading `-` excludes — so `memory -windows` and
`"event log", prefetch` both do what they look like. Terms as short as two characters work.
A query that finds nothing offers the nearest indexed terms rather than generic examples.

Suggestions are keyboard-navigable; Enter commits what you typed unless you explicitly
highlight a suggestion first.

## Contributing

Open an issue or PR with the tool's URL and a sentence on what it does and when you would
reach for it. Useful additions are tools that fill a real gap; descriptions should say what
a tool is *for* rather than list its features.

Corrections are just as welcome — a platform tag that is wrong, a link that has moved, a
tool in a category where nobody would look for it.

## Licence

Content is [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — reuse, adapt and
redistribute freely, including commercially, with attribution. Linked tools remain the
property of their authors and carry their own licences.
