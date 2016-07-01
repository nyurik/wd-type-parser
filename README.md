# wd-type-parser
Given a value object as returned from Wikidata Query Service, returns a simplified value

```lang=js
wtp = require('wd-type-parser');

// 'Q12345'
wtp({ type:'uri', value:'http://www.wikidata.org/entity/Q12345' });

// [-64.2, -36.62]
wtp({ type:'literal', datatype:'http://www.opengis.net/ont/geosparql#wktLiteral', value:'Point(-64.2 -36.62)' });

// 42
wtp({ type:'literal', datatype:'http://www.w3.org/2001/XMLSchema#integer', value:'42' });

```
