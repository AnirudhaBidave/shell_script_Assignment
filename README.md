# shell_script_Assignment
```bash
#! /bin/bash
limit=10
read cname scale view count
if [[ "$cname" -eq 'INGESTOR'||'JOINER'||'WRANGLER'||'VALIDATOR' ]] && [[ "$scale" -eq 'MID'||'HIGH'||'LOW' ]] && [[ "$view" -eq 'Auction'||'Bid' ]] && [[ "$count" -lt "$limit" ]]
then
   echo "$view;$scale;$cname;ETL;vdopia-etl=$count" > sig.conf
else
   echo "Enter valid Input"
fi```
