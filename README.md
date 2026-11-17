## Monitoring Profiles with Pyroscope and Grafana  


Below is the complete setup how to use Grafana Pyroscope and Grafana to collect, store, and view profiling data (such as flame graphs).

To simplify the setup, I use docker images to demotrate traces in Grafana webpage.  

**Setup**  
Run the below commands to download the demo repository and run Pyroscope and Grafana.  
```bash
#Downloading the repository
git clone git@github.com:hiepdng/monitoring_profiles_with_pyroscope_grafana.git

#Creating volumes
cd monitoring_profiles_with_pyroscope_grafana
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
- Pyroscope: http://localhost:4040/

**View Grafana Drilldown Profiles:**  
To view traces page:  
- goto http://localhost:3000/
- Click on `Drilldown` ->`Profiles`
- Make sure select `Pyroscope` as `Data source`



