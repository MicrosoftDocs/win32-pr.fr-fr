---
title: External. addToBasket, méthode
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. addToBasket, méthode
ms.assetid: c0dc8cd7-b924-47b8-b36c-caff8f1f892f
keywords:
- méthode addToBasket lecteur Windows Media
- méthode addToBasket lecteur Windows Media, classe externe
- Classe externe lecteur Windows Media, méthode addToBasket
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
ms.openlocfilehash: d2e2fab549dec9e24b0c5bbe61f5511e375c4c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540551"
---
# <a name="externaladdtobasket-method"></a>External. addToBasket, méthode

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La méthode **addToBasket** ajoute des éléments multimédias au volet Liste (également appelé panier) dans le lecteur Windows Media.

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

 

 





