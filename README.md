# Veri-Cekme
import bs4 as bs
import urllib.request
kaynak=urllib.request.urlopen('http://www.kariyer.net/is-ilanlari/izmir#&ct=c35').read()
sayfa=bs.BeautifulSoup(kaynak,'lxml')

izmir_is = sayfa.find('div', {"id":"divList"}).text
print(izmir_is)

