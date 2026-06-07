# backtrader

Lern-Notebook zum Einstieg in [`backtrader`](https://www.backtrader.com/) — ein
Python-Framework für Strategie-Backtests auf historischen Kursdaten.

Stand: 2019, nicht aktiv gepflegt. Liegt hier als Referenz.

## Was drin ist

`backtrader_alpha_1.ipynb` — ein einzelnes Jupyter-Notebook (für Colab gebaut):

1. Installiert `alpha_vantage` + `backtrader`
2. Lädt Daily-OHLCV via Alpha-Vantage-API
3. Backtestet eine simple RSI-Mean-Reversion-Strategie:
   - **Entry:** RSI(21) < 25 → Long 100 Stück
   - **Exit:** RSI(21) > 40 → Close

Default-Ticker: `VOE.VIE` (Voestalpine, Wiener Börse), Zeitfenster
2019-01-01 bis 2019-08-28. Beides ist im Notebook hartkodiert.

Der Strategie-Code basiert auf einem Beispiel von
[backtest-rookies.com](https://backtest-rookies.com/) (MIT, Copyright-Header
im Notebook).

## Benutzung

In Colab oder lokal mit Jupyter öffnen, eigenen Alpha-Vantage-API-Key in
Zelle 2 (`Apikey = '...'`) eintragen und alle Zellen ausführen.

API-Key kostenlos unter <https://www.alphavantage.co/support/#api-key>.

## Abhängigkeiten

```
pip install alpha_vantage backtrader
```

Notebook wurde gegen `alpha_vantage 2.1.0` / `backtrader 1.9.74.123` /
Python 3.6 (Colab 2019) erstellt — aktuelle Versionen sollten auch laufen.

## Hinweis zum API-Key

Im ursprünglich committeten Notebook war ein Alpha-Vantage-API-Key
hardcoded. Der Key ist seit 2019 öffentlich und sollte als verbrannt
betrachtet werden — vor Wiederverwendung des Notebooks einen neuen Key
generieren.
