---
title: WMPEFFECTS
description: Il s’agit d’effets prédéfinis avec les valeurs par défaut suivantes.
ms.assetid: ebee17e3-96b0-4748-b69f-4ff41d0bc386
keywords:
- WMPEFFECTS Lecteur Windows Media
topic_type:
- apiref
api_name:
- WMPEFFECTS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e84f33833e9d69c39cb50ff81bd6c97ff8f79d1e2f881f82d6e4d293e78d87bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761269"
---
# <a name="wmpeffects"></a>WMPEFFECTS

Il s’agit d' **effets** prédéfinis avec les valeurs par défaut suivantes.

``` syntax
horizontalAlignment="stretch"
verticalAlignment="stretch"
height="200"
width="250"
tabStop="false"
onclick="next();"
```

## <a name="remarks"></a>Remarques

Cela crée un élément **Effects** qui parcourt les présélections de visualisation lorsque l’utilisateur clique sur le contrôle. Elle étend également les visualisations lorsque le joueur est redimensionné.

La présélection de visualisation initiale présentée est celle sélectionnée dans le menu **affichage** sous **visualisations**. La modification de la sélection dans ce menu entraîne automatiquement la modification de la présélection affichée par cet élément lorsque le joueur est en mode apparence. Le menu **affichage** est affiché en mode complet du lecteur ou lorsque l’attribut **View. TitleBar** a la valeur true dans une apparence.

Toutes les propriétés de cet élément **Effects** peuvent être remplacées en les spécifiant explicitement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------|
| Version<br/> | Lecteur Windows Media 7,0 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EFFECTs**](effects-element.md)
</dt> </dl>

 

 





