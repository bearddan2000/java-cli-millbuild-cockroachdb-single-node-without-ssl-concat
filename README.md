# java-cli-millbuild-cockroachdb-single-node-without-ssl-concat

## Description
Creates a small database table
called `dog`. This table, `dog`, has been normalized to 3NF.
Two new tables have been added, `breedLookup` and `colorLookup`.
Creates a new table `dog_expanded` that joins
`dog`, `breedLookup` and `colorLookup`.

Turned `dog_expanded` into a view with an
implicit index on `dog_expanded`.id. Using a subquery with the aggregate function COUNT, create a new view `breed_count`.

Create a new view `dog_final` based on `breed_count`

All output normally
seen in a terminal will be in `log` which will dump to the screen. The project may seem to hang but the logs from the container must be written to the project this can take up to 3 min.

A java gradle build, that connects to single node
cockroach database without ssl.

## Tech stack
- java
- millbuild
  - postgres drivers

## Docker stack
- cockroachdb/cockroach:v19.2.2
- nightscape/scala-mill

## To run
`sudo ./install.sh -u`
- [webui](http://localhost:8080)

## To stop
`sudo ./install.sh -d`

## For help
`sudo ./install.sh -h`

## Credit
[Cockroach setup](https://github.com/s0rg/cockroach-compose)
