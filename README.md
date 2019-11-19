# country-flags-onefile
Colección de Banderas de todos los países en un solo archivo CSS y PNG

## Instalación

Usted debe [descargar](https://github.com/alainrc2005/country-flags-onefile/archive/master.zip)
todo el proyecto o instalar vía NPM:

```bash
$ npm install @alainrc2005/country-flags-onefile
```

## Uso

Para el uso solamente tiene que agregar las clasess `.flag` y `.flag-xx` (donde `xx` es el código de 2
 caracteres [ISO 3166-1-alpha-2 code](https://www.iso.org/obp/ui/#search/code/)
de un país) a un `<span>`, `<i>`, etc. Ejemplo:

```html
<span class="flag flag-cu"></span>
```

## Ejemplo utilizando quasar en una SPA con Laravel

Agregar al resources\sass\app.scss @import '~@alainrc2005/country-flags-onefile/css/flags-24x24.css'; 

```js

<template>
...

<q-select debounce="1000" v-model="country" label="Seleccione País"
    options="countries"
    option-value="value"
    map-options
    emit-value
    hide-bottom-space
    options-dense
    behavior="menu">
        <template v-slot:selected-item="scope">
            <div class="flag " :class="'flag-'+scope.opt.value"></div>&nbsp;{{scope.opt.label}}
        </template>
        <template v-slot:option="scope">
            <q-item
                v-bind="scope.itemProps"
                v-on="scope.itemEvents"
                >
                    <q-item-section>
                        <div class="flag" :class="'flag-'+scope.opt.value"></div>
                    </q-item-section>
                    <q-item-section>
                        <q-item-label v-html="scope.opt.label"></q-item-label>
                    </q-item-section>
            </q-item>
        </template>
</q-select>
							
...
</template>

...
data() {
            return { 
			  country: null,
			  countries: [
                {label: "Afghanistan", value: "af"},
                {label: "Albania", value: "al"},
                {label: "Algeria", value: "dz"},
                {label: "Andorra", value: "ad"},
                {label: "Angola", value: "ao"},
                {label: "Antigua and Barbuda", value: "ag"},
                {label: "Argentina", value: "ar"},
                {label: "Armenia", value: "am"},
                {label: "Australia", value: "au"},
                {label: "Austria", value: "at"},
                {label: "Azerbaijan", value: "az"},
                {label: "Bahamas", value: "bs"},
                {label: "Bahrain", value: "bh"},
                {label: "Bangladesh", value: "bd"},
                {label: "Barbados", value: "bb"},
                {label: "Belarus", value: "by"},
                {label: "Belgium", value: "be"},
                {label: "Belize", value: "bz"},
                {label: "Benin", value: "bj"},
                {label: "Bhutan", value: "bt"},
                {label: "Bolivia (Plurinational State of)", value: "bo"},
                {label: "Bosnia and Herzegovina", value: "ba"},
                {label: "Botswana", value: "bw"},
                {label: "Brazil", value: "br"},
                {label: "Brunei Darussalam", value: "bn"},
                {label: "Bulgaria", value: "bg"},
                {label: "Burkina Faso", value: "bf"},
                {label: "Burundi", value: "bi"},
                {label: "Cabo Verde", value: "cv"},
                {label: "Cambodia", value: "kh"},
                {label: "Cameroon", value: "cm"},
                {label: "Canada", value: "ca"},
                {label: "Central African Republic", value: "cf"},
                {label: "Chad", value: "td"},
                {label: "Chile", value: "cl"},
                {label: "China", value: "cn"},
                {label: "Colombia", value: "co"},
                {label: "Comoros", value: "km"},
                {label: "Congo", value: "cg"},
                {label: "Congo, Democratic Republic of the", value: "cd"},
                {label: "Costa Rica", value: "cr"},
                {label: "Côte d'Ivoire", value: "ci"},
                {label: "Croatia", value: "hr"},
                {label: "Cuba", value: "cu"},
                {label: "Cyprus", value: "cy"},
                {label: "Czechia", value: "cz"},
                {label: "Denmark", value: "dk"},
                {label: "Djibouti", value: "dj"},
                {label: "Dominica", value: "dm"},
                {label: "Dominican Republic", value: "do"},
                {label: "Ecuador", value: "ec"},
                {label: "Egypt", value: "eg"},
                {label: "El Salvador", value: "sv"},
                {label: "Equatorial Guinea", value: "gq"},
                {label: "Eritrea", value: "er"},
                {label: "Estonia", value: "ee"},
                {label: "Eswatini", value: "sz"},
                {label: "Ethiopia", value: "et"},
                {label: "Fiji", value: "fj"},
                {label: "Finland", value: "fi"},
                {label: "France", value: "fr"},
                {label: "Gabon", value: "ga"},
                {label: "Gambia", value: "gm"},
                {label: "Georgia", value: "ge"},
                {label: "Germany", value: "de"},
                {label: "Ghana", value: "gh"},
                {label: "Greece", value: "gr"},
                {label: "Grenada", value: "gd"},
                {label: "Guatemala", value: "gt"},
                {label: "Guinea", value: "gn"},
                {label: "Guinea-Bissau", value: "gw"},
                {label: "Guyana", value: "gy"},
                {label: "Haiti", value: "ht"},
                {label: "Honduras", value: "hn"},
                {label: "Hungary", value: "hu"},
                {label: "Iceland", value: "is"},
                {label: "India", value: "in"},
                {label: "Indonesia", value: "id"},
                {label: "Iran (Islamic Republic of)", value: "ir"},
                {label: "Iraq", value: "iq"},
                {label: "Ireland", value: "ie"},
                {label: "Israel", value: "il"},
                {label: "Italy", value: "it"},
                {label: "Jamaica", value: "jm"},
                {label: "Japan", value: "jp"},
                {label: "Jordan", value: "jo"},
                {label: "Kazakhstan", value: "kz"},
                {label: "Kenya", value: "ke"},
                {label: "Kiribati", value: "ki"},
                {label: "Korea (Democratic People's Republic of)", value: "kp"},
                {label: "Korea, Republic of", value: "kr"},
                {label: "Kuwait", value: "kw"},
                {label: "Kyrgyzstan", value: "kg"},
                {label: "Lao People's Democratic Republic", value: "la"},
                {label: "Latvia", value: "lv"},
                {label: "Lebanon", value: "lb"},
                {label: "Lesotho", value: "ls"},
                {label: "Liberia", value: "lr"},
                {label: "Libya", value: "ly"},
                {label: "Liechtenstein", value: "li"},
                {label: "Lithuania", value: "lt"},
                {label: "Luxembourg", value: "lu"},
                {label: "Madagascar", value: "mg"},
                {label: "Malawi", value: "mw"},
                {label: "Malaysia", value: "my"},
                {label: "Maldives", value: "mv"},
                {label: "Mali", value: "ml"},
                {label: "Malta", value: "mt"},
                {label: "Marshall Islands", value: "mh"},
                {label: "Mauritania", value: "mr"},
                {label: "Mauritius", value: "mu"},
                {label: "Mexico", value: "mx"},
                {label: "Micronesia (Federated States of)", value: "fm"},
                {label: "Moldova, Republic of", value: "md"},
                {label: "Monaco", value: "mc"},
                {label: "Mongolia", value: "mn"},
                {label: "Montenegro", value: "me"},
                {label: "Morocco", value: "ma"},
                {label: "Mozambique", value: "mz"},
                {label: "Myanmar", value: "mm"},
                {label: "Namibia", value: "na"},
                {label: "Nauru", value: "nr"},
                {label: "Nepal", value: "np"},
                {label: "Netherlands", value: "nl"},
                {label: "New Zealand", value: "nz"},
                {label: "Nicaragua", value: "ni"},
                {label: "Niger", value: "ne"},
                {label: "Nigeria", value: "ng"},
                {label: "North Macedonia", value: "mk"},
                {label: "Norway", value: "no"},
                {label: "Oman", value: "om"},
                {label: "Pakistan", value: "pk"},
                {label: "Palau", value: "pw"},
                {label: "Panama", value: "pa"},
                {label: "Papua New Guinea", value: "pg"},
                {label: "Paraguay", value: "py"},
                {label: "Peru", value: "pe"},
                {label: "Philippines", value: "ph"},
                {label: "Poland", value: "pl"},
                {label: "Portugal", value: "pt"},
                {label: "Qatar", value: "qa"},
                {label: "Romania", value: "ro"},
                {label: "Russian Federation", value: "ru"},
                {label: "Rwanda", value: "rw"},
                {label: "Saint Kitts and Nevis", value: "kn"},
                {label: "Saint Lucia", value: "lc"},
                {label: "Saint Vincent and the Grenadines", value: "vc"},
                {label: "Samoa", value: "ws"},
                {label: "San Marino", value: "sm"},
                {label: "Sao Tome and Principe", value: "st"},
                {label: "Saudi Arabia", value: "sa"},
                {label: "Senegal", value: "sn"},
                {label: "Serbia", value: "rs"},
                {label: "Seychelles", value: "sc"},
                {label: "Sierra Leone", value: "sl"},
                {label: "Singapore", value: "sg"},
                {label: "Slovakia", value: "sk"},
                {label: "Slovenia", value: "si"},
                {label: "Solomon Islands", value: "sb"},
                {label: "Somalia", value: "so"},
                {label: "South Africa", value: "za"},
                {label: "South Sudan", value: "ss"},
                {label: "Spain", value: "es"},
                {label: "Sri Lanka", value: "lk"},
                {label: "Sudan", value: "sd"},
                {label: "Suriname", value: "sr"},
                {label: "Sweden", value: "se"},
                {label: "Switzerland", value: "ch"},
                {label: "Syrian Arab Republic", value: "sy"},
                {label: "Tajikistan", value: "tj"},
                {label: "Tanzania, United Republic of", value: "tz"},
                {label: "Thailand", value: "th"},
                {label: "Timor-Leste", value: "tl"},
                {label: "Togo", value: "tg"},
                {label: "Tonga", value: "to"},
                {label: "Trinidad and Tobago", value: "tt"},
                {label: "Tunisia", value: "tn"},
                {label: "Turkey", value: "tr"},
                {label: "Turkmenistan", value: "tm"},
                {label: "Tuvalu", value: "tv"},
                {label: "Uganda", value: "ug"},
                {label: "Ukraine", value: "ua"},
                {label: "United Arab Emirates", value: "ae"},
                {label: "United Kingdom of Great Britain and Northern Ireland", value: "gb"},
                {label: "United States of America", value: "us"},
                {label: "Uruguay", value: "uy"},
                {label: "Uzbekistan", value: "uz"},
                {label: "Vanuatu", value: "vu"},
                {label: "Venezuela (Bolivarian Republic of)", value: "ve"},
                {label: "Viet Nam", value: "vn"},
                {label: "Yemen", value: "ye"},
                {label: "Zambia", value: "zm"},
                {label: "Zimbabwe", value: "zw"},
                ]
		}
	}
```

