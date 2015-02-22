ISO 3166
============
Get localized country names from ISO 3166-1 codes.



### How use?
##### INIT
~~~~~~ php
use CountryIso\ISO3166;

$isoCodes = new ISO3166();
~~~~~

##### SET COUNTRIES ALIASES
~~~~~~ php
// Add an alias for the Vatican
$countryCodes->setCountriesAliases([
    'VA' => 'Vatican'
]);
// or add some aliases for the Vatican
$countryCodes->setCountriesAliases([
    'VA' => [
        'Holy See',
        'Vatican',
        'Vatican City State'
    ]
]);
~~~~~

##### GET DATA
Get country name by code:
~~~~~~ php
echo $countryCodes->getCountry("US");  // United States
echo $countryCodes->getCountry("UA");  // Ukraine
echo $countryCodes->getCountry("ES");  // Spain
~~~~~

Get country code by name or aliases:
~~~~~~ php
echo $countryCodes->getCountry("Ukraine");      // UA
echo $countryCodes->getCountry("United States");// US

echo $countryCodes->getCountry("Vatican");      // VA
echo $countryCodes->getCountry("Holy See");     // VA
~~~~~

Get map (all countries array):
~~~~~~ php
$allCountries = $countryCodes->getMap();
~~~~~~
