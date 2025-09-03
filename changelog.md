# Changelog 

This changelog reflects modifications made to the source ISO datasheets in order to make this dataset a useful lookup reference for most mainstream analytical contexts. 

The objective of this dataset is to consolidate ISO-3166 (countries) and ISO-4127 (currencies) to provide a quick reference single dataset to answer questions like:

- What's the ISO code for Australia and what's the currency code for the Australian Dollar?

For that reason, various currencies provided by ISO-4217 but not the national currency were removed (see the `edited` vs `original` split in source). 

Specifically these were the special settlement units (Chile's CLF, IMF's XDR) given that these are not legal tender in specific countries. 


## Removed From ISO 4217 (Currencies)


Antartica (no currency)

### Other Removals

Specialised instruments not country specific

INTERNATIONAL MONETARY FUND (IMF) ,SDR (Special Drawing Right),XDR,960

MEMBER COUNTRIES OF THE AFRICAN DEVELOPMENT BANK GROUP,ADB Unit of Account,XUA,965

"SISTEMA UNITARIO DE COMPENSACION REGIONAL DE PAGOS ""SUCRE""",Sucre,XSU,994

ARAB MONETARY FUND,Arab Accounting Dinar,XAD,396

Commodities

Also:

UNITED STATES OF AMERICA (THE),US Dollar (Next day),USN,997

## September 2025 updates

- El Salvador: removed SVC (El Salvador Colon) as deprecated; USD only.
- Bolivia: removed BOV (Mvdol) settlement unit.
- Chile: removed CLF (Unidad de Fomento) settlement unit.
- Colombia: removed COU (Unidad de Valor Real) settlement unit.
- Mexico: removed MXV (Mexican Unidad de Inversion (UDI)) settlement unit.
- Uruguay: removed UYI (UI) indexed unit.
- Switzerland: removed CHE (WIR Euro) and CHW (WIR Franc); CHF only.
