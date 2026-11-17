## Monitoring Profiles with Pyroscope and Grafana  


Below is the complete setup how to use Grafana Pyroscope and Grafana to collect, store, and view profiling data (such as flame graphs).

To simplify the setup, I use docker images to demotrate traces in Grafana webpage.  

**Setup**  
Run the below commands to download the demo repository and run Pyroscope, Tempo and Grafana.  
```bash
#Downloading the repository
git clone git@github.com:hiepdng/monitoring_profiles_with_pyroscope_grafana.git

#Creating volumes
cd monitoring_traces_with_alloy_tempo_grafana
mkdir grafana_data
sudo chown -R 472:472 grafana_data
mkdir pyroscope_data
sudo chown -R 10001:10001 pyroscope_data

#Running containers
docker compose up -d
```
**Access Grafana web:**  
Go to http://localhost:3000/ to access your local Grafana webpage and view the host and containers metrics.  

To view specific container webpages:  
- Alloy: http://localhost:12345
- Tempo: http://localhost:3200/ready or http://localhost:3200/metrics

**View Grafana Drilldown Traces:**  
To view traces page:  
- goto http://localhost:3000/
- Click on `Drilldown` ->`Traces`
- Make sure select `Tempo` as `Data source`



