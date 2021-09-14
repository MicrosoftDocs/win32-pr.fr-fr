---
description: La propriété ProductLanguage doit être mise à jour vers l’identificateur de langue numérique (LANGID) pour la nouvelle langue.
ms.assetid: e00ef69b-c54b-41de-9230-a7582b260891
title: Mise à jour des propriétés ProductLanguage et ProductCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a7537cdb0295075fbfd1b8b58e45a051610cf6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223097"
---
# <a name="updating-productlanguage-and-productcode-properties"></a>Mise à jour des propriétés ProductLanguage et ProductCode

La propriété [**ProductLanguage**](productlanguage.md) doit être mise à jour vers l’identificateur de langue numérique (LANGID) pour la nouvelle langue. Dans le cas de l’exemple de localisation, la valeur de la propriété **ProductLanguage** doit être remplacée par celle de l’anglais (1033) par celle de l’ID de langue français (1036) dans la [table des propriétés](property-table.md).

La valeur de la propriété [**ProductCode**](productcode.md) dans la [table de propriétés](property-table.md) doit être remplacée par une nouvelle valeur unique lors de la localisation d’une base de données, car un produit localisé est considéré comme un produit différent. Par exemple, les versions allemande et anglaise d’une application sont considérées comme deux produits différents et doivent avoir des codes de produit différents. Consultez la section [codes de produit](product-codes.md).

Utilisez votre éditeur de table de base de données pour mettre à jour les valeurs des propriétés ProductCode et ProductLanguage dans la table de propriétés. Ne réutilisez pas le GUID affiché si vous copiez cet exemple.

[Table de propriétés](property-table.md)



| Propriété                                   | Valeur                                  |
|--------------------------------------------|----------------------------------------|
| [**ProductCode**](productcode.md)         | {EE389960-E426-4EEA-B669-AD8129249881} |
| [**ProductLanguage**](productlanguage.md) | 1036                                   |



 

[Continuer](updating-a-summary-information-stream.md)

 

 



