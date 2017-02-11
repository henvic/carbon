# Carbon

HTTP Response Header Filtering

> carbon filtering: method of filtering impurities

## Build

To build and install the `carbon` executable run:

```bash
make install
```

> this will install to `/usr/local/bin`

## Usage

Help...

```bash
carbon -help
  
  -filter string
        comma-separated list of headers to be displayed
        e.g. X-Siterouter-Upstream,X-Cache
  -help
        show commands
```

With filter...

```bash
carbon -filter X-Cache https://www.buzzfeed.com/

  X-Cache:
    [HIT]

  Status Code: 200 OK
```

No filter...

```bash
carbon https://www.buzzfeed.com/

Accept-Ranges:
  [bytes]

Age:
  [47]

Cache-Control:
  [no-cache, no-store, must-revalidate]

...lots of stuff...

X-Timer:
  [S1486813451.981669,VS0,VE0]

Status Code: 200 OK
```

## Tests?

Nope. This was just a quick hack