---
title: External. selectedItemID
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. selectedItemID
ms.assetid: 150aaa38-d4fe-493e-bda1-e5b0a27fccf7
keywords:
- External. selectedItemID Lecteur Windows Media
topic_type:
- apiref
api_name:
- External.selectedItemID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea4b93656adc3fab25ab96e41fe417bde158035c5c11a0af9be84c5d555b153
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648429"
---
# <a name="externalselecteditemid"></a>External. selectedItemID

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

la propriété **selectedItemID** récupère l’identificateur de l’élément multimédia actuellement sélectionné dans Lecteur Windows Media.

## <a name="syntax"></a>Syntaxe

``` syntax
window.external.selectedItemID
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture seule.

## <a name="remarks"></a>Remarques

Cette propriété est utilisée en association avec la propriété [External. selectedItemType](external-selecteditemtype.md) . Par exemple, si **selectedItemType** est égal à CPTrackID, **SELECTEDITEMID** est l’ID de la piste sélectionnée. pour plus d’informations sur la façon dont Lecteur Windows Media caractérise les vues du contenu du magasin en ligne, consultez [emplacement et élément sélectionné](location-and-selected-item.md).

certains affichages dans Lecteur Windows Media ont un élément multimédia spécifique qui est sélectionné. Par exemple, supposons que la vue actuelle représente un album. Un album est un conteneur de pistes. par conséquent, **selectedItemType** est égal à CPTrackID et **SELECTEDITEMID** est l’ID de la piste sélectionnée. Les autres vues n’ont pas d’élément multimédia sélectionné. par exemple, si l’utilisateur clique sur le nœud racine du magasin en ligne dans le contrôle tree-view, Lecteur Windows Media affiche une page de détection fournie par le magasin en ligne. Le lecteur n’affiche aucun conteneur d’éléments multimédias dans l’interface utilisateur du lecteur. Dans ce cas, **selectedItemType** est égal à UnknownLocation et **SelectedItemId** est égal à la chaîne vide.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. selectedItemType**](external-selecteditemtype.md)
</dt> <dt>

[**Emplacement et élément sélectionné**](location-and-selected-item.md)
</dt> </dl>

 

 





