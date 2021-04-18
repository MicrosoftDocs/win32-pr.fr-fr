---
description: Le kit de développement logiciel (SDK) Microsoft Windows comprend des chaînes de ressources localisées, des tables d’erreurs localisées et des tables ActionText localisées pour les langues listées dans le tableau ci-dessous.
ms.assetid: 2e3a6e73-5b06-452d-9f87-18eb6914b961
title: Localisation des tables Error et ActionText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c45428d9f0d3c4b8dcafbf489f7316225a83f032
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319502"
---
# <a name="localizing-the-error-and-actiontext-tables"></a>Localisation des tables Error et ActionText

Le kit de développement logiciel (SDK) Microsoft Windows comprend des chaînes de ressources localisées, des [tables d’erreurs](error-table.md)localisées et des [tables ActionText](actiontext-table.md) localisées pour les langues listées dans le tableau ci-dessous. Les langues indiquées par des astérisques indiquent que les chaînes de ressources sont stockées en tant que langue de base et peuvent donc être utilisées avec tous les dialectes de cette langue.

Vous pouvez importer les tables Error et ActionText localisées dans votre base de données à l’aide de Msidb.exe ou [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).



| LANGID (décimal) | LANGID (hexadécimal) | Page de codes ASCII | Abréviation | Language                      | Language-Culture |
|------------------|----------------------|-----------------|--------------|-------------------------------|------------------|
| 1025\*           | 0x401                | 1256            | ARA          | Arabe - Arabie saoudite         | ar-SA            |
| 1027             | 0x403                | 1252            | CHATS          | Catalan                       | ca-ES            |
| 1028\*           | 0x404                | 950             | CHT          | Chinois - Taïwan              | zh-TW            |
| 2052             | 0x804                | 936             | CHS          | Chinois - Chine               | zh-CN            |
| 1029             | 0x405                | 1250            | CSY          | Tchèque-République tchèque        | cs-CZ            |
| 1030             | 0x406                | 1252            | DAN          | Danois-Danemark               | da-DK            |
| 1031\*           | 0x407                | 1252            | DEU          | Allemand – Allemagne              | de-DE            |
| 1032             | 0x408                | 1253            | ELL          | Grec-Grèce                | el-GR            |
| 1033\*           | 0x409                | 1252            | ENU          | French - France       | fr-FR            |
| 3082\*           | 0xC0A                | 1252            | ESN          | Espagnol-moderne-tri-Espagne | es-ES            |
| 1061             | 0x425                | 1257            | ETI          | Estonien                      | Et-EE            |
| 1035             | 0x40B                | 1252            | FIN          | Finnois-Finlande             | fi-FI            |
| 1036\*           | 0x40C                | 1252            | FRA          | Français – France               | fr-FR            |
| 1037             | 0x40D                | 1 255            | HEB          | Hébreu-Israël               | he-IL            |
| 1038             | 0x40E                | 1250            | HUN          | Hongrois-Hongrie           | hu-HU            |
| 1040\*           | 0x410                | 1252            | ITA          | Italien - Italie               | it-IT            |
| 1041             | 0x411                | 932             | JPN          | Japonais – Japon              | jp-JP            |
| 1042             | 0x412                | 949             | KOR          | Coréen – Corée                | Ko-KO            |
| 1063             | 0x427                | 1257            | LTH          | Lituanien                    | lt-LT            |
| 1062             | 0x426                | 1257            | LVI          | Letton                       | lv-LV            |
| 1043\*           | 0x413                | 1252            | NLD          | Néerlandais - Pays-bas           | nl-NL            |
| 1044\*           | 0x414                | 1252            | NOR          | Norvégien (Bokmål)-Norvège    | nb-NO            |
| 1045             | 0x415                | 1250            | PLK          | Polonais-Pologne               | pl-PL            |
| 1046             | 0x416                | 1252            | PTB          | Portugais - Brésil           | pt-br            |
| 2070             | 0x816                | 1252            | PTG          | Portugais - Portugal         | pt-PT            |
| 1048             | 0x418                | 1250            | ROM          | Roumain-Roumanie            | ro-RO            |
| 1049             | 0x419                | 1251            | RUS          | Russe – Russie              | ru-RU            |
| 1050             | 0x41A                | 1250            | HRV          | Croate-Croatie            | hr-HR            |
| 1051             | 0x41B                | 1250            | CIEL          | Slovaque-Slovaquie             | sk-SK            |
| 1053\*           | 0x41D                | 1252            | SVE          | Suédois-Suède              | sv-SE            |
| 1054             | 0x41E                | 874             | THA          | Thaï-Thaïlande               | th-TH            |
| 1055             | 0x41F                | 1254            | TRK          | Turc-Turquie              | tr-TR            |
| 1060             | 0x424                | 1250            | SLV          | Slovène-Slovénie          | sl-SI            |
| 1066             | 0x42A                | 1258            | VIT          | Vietnamien-Viêt Nam         | vi-VN            |
| 1069             | 0x42D                | 1252            | EUQ          | Basque (Basque)               | eu-ES            |



 

**Windows Vista :** Outre les langues répertoriées dans le tableau précédent, les langues répertoriées dans le tableau suivant sont disponibles à partir de Windows Vista.



| LANGID (décimal) | LANGID (hexadécimal) | Page de codes ASCII | Abréviation | Language        | Language-Culture |
|------------------|----------------------|-----------------|--------------|-----------------|------------------|
| 1026             | 0x402                | 1251            | BVR          | Bulgare       | bg-BG            |
| 1058             | 0x422                | 1251            | UKR          | Ukrainien       | uk-UA            |
| 2074             | 0x81A                | 1250            | SRL          | Serbe (latin) | SR-LATN-CS       |



 

 

 



