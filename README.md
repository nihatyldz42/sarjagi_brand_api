

## API Bağlantıları
Api deneme amaçlı olduğu için herhangi bir token belirtecine gerek yoktur.


# Yol Üzeri İstasyonlara Erişim
Yol üzerindeki en yakın istasyonların verisini döndürür.
Sıralama yukarıdan aşağı şeklindedir.

```http
  POST https://sarjagi.com/api/brand/onroad
```

### Parametreler (application/json şeklinde)
```json
  {
    "locationIn" : [ //başlangıç konumu
        41.750115, //lat
        26.655103 //long
    ],
    "locationOut" : [ //bitiş konumu
        39.6829002, //lat
        34.4581702 //long
    ]
}
```

### Çıktı
```json
[
    {
        "loc": {
            "type": "Point",
            "coordinates": [
                31.49578,
                39.865995
            ]
        },
        "_id": "620cc01320e316f1dd751f2e",
        "title": "MihalÄ±cÃ§Ä±k Belediyesi ",
        "address": "Camikebir Mah. ÃmerkÃ¶y Cad. No:33",
        "note": "Belediye Ã¶nÃ¼ aÃ§Ä±k otopark saÄ taraf",
        "usage_hours": "00:00-24:00",
        "parking_slots": "2",
        "tariff_information": "Ãcretli KullanÄ±m",
        "nearby_places": "-",
        "sockets": [
            "-",
            "-",
            "1 Soket </br> 22 kW"
        ],
        "type": "AC",
        "like": "0",
        "station_owner": "zes",
        "station_code": "MHLÃKBLDY-AC1",
        "__v": 0,
        "updatedAt": "2022-06-20T09:03:33.482Z"
    },
    {
        "loc": {
            "type": "Point",
            "coordinates": [
                32.661659,
                40.467954
            ]
        },
        "_id": "620cc01220e316f1dd751c58",
        "title": "Ankara Eliz Hotel ",
        "address": " Ä°smetpaia Mah. 1. Cad. KÄ±zÄ±lcahamam/Ankara",
        "note": "Otel giriÅinin karÅÄ±sÄ±",
        "usage_hours": "00:00-24:00",
        "parking_slots": "2",
        "tariff_information": "Ãcretli KullanÄ±m",
        "nearby_places": "-",
        "sockets": [
            "-",
            "-",
            "2 Soket </br> 22 kW"
        ],
        "type": "AC",
        "like": "0",
        "station_owner": "zes",
        "station_code": "ANKELÄ°ZHOT-AC1",
        "__v": 0,
        "updatedAt": "2022-06-20T09:03:33.474Z"
    },
    ....
]
```



# Tüm İstasyonlara Erişim
Sunucumuzda kayıtlı tüm güncel istasyonları döndürür.
```http
  GET /api/brand/all
```

# Yakın İstasyonlara Erişim
Belirtilmiş konuma en yakın istasyonları döndürür.
#### lg = boylam / longitude
#### lt = enlem / latiude
#### distance = metre bazında yarıçap

```http
  GET /api/brand/near?lg=32.661659&lt=40.467954&distance=1000
```



