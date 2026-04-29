ES vježba

Ovaj projekt prikazuje rad s Elasticsearchom i Kibanom kroz praktične zadatke i HTTP upite zapisane u datoteci queries.http
Pokretanje okruženja

Za pokretanje projekta potrebno je imati instalirano:
   - Docker
   - Docker Compose

Pokretanje servisa:
  docker compose up -d

Zaustavljanje:
  docker compose down

Provjera rada:
  docker compose ps
  curl http://localhost:9200/_cat/health?v

Ako je sve ispravno pokrenuto:
    - Elasticsearch je dostupan na http://localhost:9200
    - Kibana na http://localhost:5601
    
Sadržaj repozitorija
    docker-compose.yml – konfiguracija za pokretanje Elasticsearcha i Kibane
    queries.http – svi korišteni upiti 
    ODGOVORI.md – odgovori na teorijska pitanja
    images/ – slike rezultata zadataka
    README.md – osnovne upute za korištenje projekta
    
