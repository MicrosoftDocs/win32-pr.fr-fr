---
description: La clé de Registre EUDCCodeRange définit les plages de codes de caractères définis par l’utilisateur final (EUDC) pour diverses pages de codes (jeux de caractères).
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: EUDCCodeRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f20dad72012a15f6f9b9d6db29d9dfea50b4dbf4068588f679b26b144f63036a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068229"
---
# <a name="eudccoderange"></a>EUDCCodeRange

La clé de Registre EUDCCodeRange définit les plages de codes de [caractères définis par l’utilisateur final (EUDC)](end-user-defined-characters.md) pour diverses pages de codes (jeux de caractères). Elle est utilisée uniquement par les outils qui créent des EUDCs et n’est pas d’une préoccupation directe pour les utilisateurs EUDC. Cette clé de registre a l’emplacement de Registre suivant :

HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ contrôler \\ la \\ page de codes nls \\ EUDCCodeRange

Le format est le suivant :

EUDCCodeRange CodePage = FromTo \[ , FromTo\]

où :



| Valeur         | Description                                                                                                                                                                                                         |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CodePage | L’une des chaînes « 932 » (japonais), « 936 » (chinois simplifié), « 949 » (coréen), « 950 » (chinois traditionnel) ou « Unicode » (Unicode). Aucune autre valeur n’est prise en charge.                                     |
| FromTo   | Valeur de chaîne composée d’une paire de valeurs hexadécimales à 4 chiffres séparés par un trait d’Union (-). Vous pouvez spécifier jusqu’à quatre valeurs FromTo, mais chacune d’elles doit être séparée de la valeur précédente par une virgule (,). |



 

Les valeurs suivantes sont correctes pour l’entrée de registre.


```C++
932=F040-F9FC
936=A140-A7A0,AAA1-AFFE,F8A1-FEFE
949=C9A1-C9FE,FEA1-FEFE
950=8140-8DFE,8E40-A0FE,C6A1-C8FE,FA40-FEFE
Unicode=E000-F8FF
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Entrées de Registre EUDC](eudc-registry-entries.md)
</dt> <dt>

[EUDC](eudc.md)
</dt> </dl>

 

 



