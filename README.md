d3maps
======

Metabolic network visualizations using d3.js.

### Generate a map

To generate a json map file from svg, run:
```Bash
python generate_map_json.py -f bigg bigg-maps/ecoli.svg 
# OR:
python generate_map_json.py -f simpheny simpheny-maps/ijo-central.svg 
```

Use the -f option to specify format, either 'BIGG' or 'SimPheny' [default].

### Flux

Flux.json is used to show flux values. The format is:

{"reaction-id1": 0.200, "reaction-id2": 0.450}

and so on. Reaction id's should match those in the map file.


### Serving the map

To run locally, you can start the python simple server in the d3maps directory

```Bash
python -m SimpleHTTPServer 8080
```

Then point your browser to http://localhost:8080/
