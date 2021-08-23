---
title: External. addToBasket, méthode
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. addToBasket, méthode
ms.assetid: c0dc8cd7-b924-47b8-b36c-caff8f1f892f
keywords:
- Lecteur Windows Media de la méthode addToBasket
- méthode addToBasket Lecteur Windows Media, classe externe
- Lecteur Windows Media de classe externe, méthode addToBasket
topic_type:
- apiref
api_name:
- External.addToBasket
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17f51cfc3df641b02a5aa3a0869e810f318357dd70ba67acb3ec2310f8a5a355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650009"
---
# <a name="externaladdtobasket-method"></a>External. addToBasket, méthode

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

la méthode **addToBasket** ajoute des éléments multimédias au volet liste (également appelé panier) dans Lecteur Windows Media.

## <a name="syntax"></a>Syntaxe


```JScript
External.addToBasket(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ViewType* \[ dans\]
</dt> <dd>

**Chaîne** qui spécifie le type d’élément ajouté au volet liste. L’appelant doit définir ce paramètre sur l’une des [constantes d’emplacement de bibliothèque](library-location-constants.md)suivantes :

CPListID

CPTrackID

CPAlbumID

CPArtist

CPGenreID

CPAlbumSubGenreID

CPRadioID

</dd> <dt>

*ViewIDs* \[ dans\]
</dt> <dd>

**Chaîne** contenant les ID, délimités par des points-virgules, des éléments à ajouter au volet de liste.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ExternalObject pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. basketTitle**](external-baskettitle.md)
</dt> </dl>

 

 





