---
description: Définit des intervalles de date et d’heure avec un format similaire à la syntaxe de date et d’heure en scindant la chaîne en champs pour les jours, les heures, les minutes, les secondes et les microsecondes.
ms.assetid: 13a3ca74-e3e9-44d7-9254-e288eb70ae4c
ms.tgt_platform: multiple
title: Format d’intervalle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30db455b6b39349b3da2f8328b22597d8b9c16c47387ba7f6b15d81e62ceb134
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318535"
---
# <a name="interval-format"></a>Format d’intervalle

WMI définit des intervalles de date et d’heure avec un format similaire à la syntaxe de date et d’heure en scindant la chaîne en champs pour les jours, les heures, les minutes, les secondes et les microsecondes.

L’exemple suivant montre le format d’un intervalle de date/heure.

``` syntax
ddddddddHHMMSS.mmmmmm:000
```

Le tableau suivant répertorie les champs de l’intervalle de date et d’heure.



| Champ    | Description                                                                                                                                                                                                                                  |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dddddddd | Huit chiffres qui représentent un nombre de jours (00000000 à 99999999).                                                                                                                                                                    |
| HH       | Heure à deux chiffres de la journée qui utilise l’horloge de 24 heures (00 à 23).                                                                                                                                                                       |
| MM       | Minutes à deux chiffres dans l’heure (00 à 59).                                                                                                                                                                                                |
| SS       | Nombre de secondes à deux chiffres dans la minute (00 à 59).                                                                                                                                                                                   |
| mmmmmm   | Nombre de microsecondes de six chiffres dans le deuxième (000000 à 999999). Votre implémentation n’est pas requise pour prendre en charge l’évaluation à l’aide de ce champ, mais ce champ doit toujours être présent pour préserver la nature de la chaîne de longueur fixe. |



 

Les intervalles ont toujours un «  : 000 » de fin comme quatre derniers caractères. En outre, contrairement à la date et à l’heure, vous ne pouvez pas utiliser d’astérisques pour indiquer les champs inutilisés. En outre, toutes les propriétés de [type \_ DateTime DateTime](cim-datetime.md) qui représentent des intervalles doivent être marquées avec le qualificateur standard [SubType](standard-wmi-qualifiers.md) , avec le qualificateur défini sur « Interval ».

La chaîne suivante représente un intervalle de 1 jour, 12 heures, 0 minute et 32 secondes.

``` syntax
00000001120032.000000:000
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format de date et d’heure](date-and-time-format.md)
</dt> <dt>

[À propos de WMI](about-wmi.md)
</dt> <dt>

[\_DateTime CIM](cim-datetime.md)
</dt> </dl>

 

 



