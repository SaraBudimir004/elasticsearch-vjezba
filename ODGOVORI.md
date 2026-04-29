1. Zeleni, žuti i crveni status u Elasticsearchu su pokazatelji stanja klastera i govore koliko je sustav trenutno ispravan i koliko su dostupni podaci.
Green znači da sve radi kako treba i svi podaci su dostupni, yellow znači da sustav radi, ali nije sve potpuno sigurno jer dio kopija podataka nije aktivan, red znači da postoji problem i da dio podataka nije dostupan ili sustav ne radi ispravno.
5.Naslov je text jer se može pretraživati po riječima,elasticsearch ga razbija na dijelove pa se može tražiti dio naslova, ne samo cijeli
6.naslov.keyword postoji za točno pretraživanje i sortiranje, tu se naslov čuva točno kako je napisan, bez dijeljenja na rijeći
7.Autor i žanr su keyword jer se traže kao točne vrijednosti, ne traži se po dijelovima nego npr. točno ime autora ili žanr(filtriranje,sortiranje...)
8.Opis je duži tekst i treba se moci pretraživati po rijecima,keyword to ne omogućuje jer ne radi analizu teksta
11. Pretraga (cuprija) pronalazi (ćuprija) jer elasticsearch mijenja slova sa kvačicama u obična slova, pa (ćuprija) postane (cuprija) i zato se poklapa s upitom
12. _score pokazuje koliko je neki rezultat dobar za ono što tražiš, šta se dokument više poklapa s upitom, to ima veci _score
Zato neki dokumenti imaju veći, a neki manji _score
U mom primjeru se vidi da je max_score null jer nema pronađenih rezultata
18. {
  "tokens": [
    {
      "token": "na",
      "start_offset": 0,
      "end_offset": 2,
      "type": "<ALPHANUM>",
      "position": 0
    },
    {
      "token": "drini",
      "start_offset": 3,
      "end_offset": 8,
      "type": "<ALPHANUM>",
      "position": 1
    },
    {
      "token": "cuprija",
      "start_offset": 9,
      "end_offset": 16,
      "type": "<ALPHANUM>",
      "position": 2
    }
  ]
}
Elasticsearch generira tokene: na, drini, cuprija-tekst je razbijen na 3 riječi,sve je pretvoreno u male znakove
19. lowercase pretvara sva slova u mala slova, a asciifolding mijenja slova s kvačicama u obična slova, razlika je u tome što lowercase mijenja samo velika slova, a asciifolding uklanja kvačice (č,ć,ž,š)->(c,z,s)

20. Analyzer je važan jer priprema tekst za pretraživanje tako da ga razbije na riječi i prilagodi (npr. mala slova, uklanjanje kvačica), bez analyzera elasticsearch bi tražio točan zapis, pa bi pretraga bila neprecizna i često ne bi pronašla rezultate ako se riječi ne poklapaju potpuno



