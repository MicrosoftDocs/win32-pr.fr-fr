---
title: StringCollection, objet
description: L’objet StringCollection fournit un moyen de manipuler une collection de chaînes.
ms.assetid: bd4f82e7-1a6a-47c5-b019-7aff520e621a
keywords:
- Objet StringCollection lecteur Windows Media
topic_type:
- apiref
api_name:
- StringCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0d1872bec7e00e87ada845f7518608ea4149f137
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104313249"
---
# <a name="stringcollection-object"></a>StringCollection, objet

L’objet **StringCollection** fournit un moyen de manipuler une collection de chaînes.

L’objet **StringCollection** prend en charge la propriété suivante.



| Propriété                            | Description                                             |
|-------------------------------------|---------------------------------------------------------|
| [count](stringcollection-count.md) | Récupère le nombre d’éléments dans la collection de chaînes. |



 

L’objet **StringCollection** prend en charge les méthodes suivantes.



| Méthode                                                                  | Description                                                                                                                     |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [getAttributeCountByType](stringcollection-getattributecountbytype.md) | Récupère le nombre d’attributs associés à l’index d’élément **StringCollection** , le nom d’attribut et la langue spécifiés. |
| [getItemInfo](stringcollection-getiteminfo.md)                         | Récupère la chaîne correspondant au nom et à l’index d’élément **StringCollection** spécifiés.                                   |
| [getItemInfoByType](stringcollection-getiteminfobytype.md)             | Récupère la chaîne correspondant à l’index d’élément **StringCollection** , au nom, à la langue et à l’index d’attribut spécifiés.       |
| [isIdentical](stringcollection-isidentical.md)                         | Récupère une valeur indiquant si l’objet fourni est identique à l’objet actuel.                                        |
| [item](stringcollection-item.md)                                       | Récupère la chaîne à l’index spécifié.                                                                                    |



 

L’objet **StringCollection** est accessible par le biais de la méthode suivante.



| Object                                        | Méthode                                                                           |
|-----------------------------------------------|----------------------------------------------------------------------------------|
| [MediaCollection](mediacollection-object.md) | [getAttributeStringCollection](mediacollection-getattributestringcollection.md) |



 

À des fins d’illustration, *joueur*. *mediaCollection*. **getAttributeStringCollection**(*attribute*, *MediaType*) est utilisé dans les sections de syntaxe de référence.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




