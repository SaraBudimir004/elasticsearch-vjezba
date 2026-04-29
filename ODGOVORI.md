1. Zeleni, žuti i crveni status u Elasticsearchu su pokazatelji stanja klastera i govore koliko je sustav trenutno ispravan i koliko su dostupni podaci.
Green znači da sve radi kako treba i svi podaci su dostupni, yellow znači da sustav radi, ali nije sve potpuno sigurno jer dio kopija podataka nije aktivan, red znači da postoji problem i da dio podataka nije dostupan ili sustav ne radi ispravno.
5.Naslov je text jer se može pretraživati po riječima,elasticsearch ga razbija na dijelove pa se može tražiti dio naslova, ne samo cijeli
6.naslov.keyword postoji za točno pretraživanje i sortiranje, tu se naslov čuva točno kako je napisan, bez dijeljenja na rijeći
7.Autor i žanr su keyword jer se traže kao točne vrijednosti, ne traži se po dijelovima nego npr. točno ime autora ili žanr(filtriranje,sortiranje...)
8.Opis je duži tekst i treba se moci pretraživati po rijecima,keyword to ne omogućuje jer ne radi analizu teksta