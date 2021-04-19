---
description: La clé de Registre EUDCCodeRange définit les plages de codes de caractères définis par l’utilisateur final (EUDC) pour diverses pages de codes (jeux de caractères).
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: EUDCCodeRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e68c71751ca5d13cd04c95ff66c84067fd1d46d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536599"
---
# <a name="eudccoderange"></a>EUDCCodeRange

La clé de Registre EUDCCodeRange définit les plages de codes de [caractères définis par l’utilisateur final (EUDC)](end-user-defined-characters.md) pour diverses pages de codes (jeux de caractères). Elle est utilisée uniquement par les outils qui créent des EUDCs et n’est pas d’une préoccupation directe pour les utilisateurs EUDC. Cette clé de registre a l’emplacement de Registre suivant :

HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ contrôler \\ la \\ page de codes nls \\ EUDCCodeRange

Le format est le suivant :

EUDCCodeRange CodePage = FromTo \[ , FromTo\]

où :



|          |                                                                                                                                                                                                          |
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

 

 



