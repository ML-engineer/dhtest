mvn compile exec:java -Dexec.mainClass=se.mathem.enrich.HitMaker -Dexec.args=" \
   --project=mathem-data \
   --stagingLocation=gs://mathem-data/dataflow/payload-enrich/staging/ \
   --runner=DataflowRunner \
   --zone=europe-west1-b \
   --numWorkers=1 \
   --maxNumWorkers=1 \
   --diskSizeGb=5 \
   --workerMachineType=n1-standard-1 \
   --pubsubTopic=projects/mathem-data/topics/measurementprotocol-1"