```sh
docker pull tile38/tile38
docker run -p 9851:9851 --name tile38 tile38/tile38
docker exec -it tile38 sh
```


```sh
ps # check if, and where tile38 is running
cd /usr/local/bin/ # optional
tile38-cli
SET fleet truck1 POINT 33.5123 -112.2693
GET fleet truck1

SETHOOK delftfence kafka://kafka:9093/tile38 NEARBY fleet FENCE POINT 52.0 4.35 5000

```
SET fleet truck1 POINT 52.0001 4.3501