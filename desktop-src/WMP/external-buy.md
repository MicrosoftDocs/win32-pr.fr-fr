---
title: External. Buy, méthode
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La méthode Buy lance l’achat d’un ensemble d’éléments multimédias.
ms.assetid: 78496de6-214e-4712-8fbc-11e002adce88
keywords:
- méthode Buy lecteur Windows Media
- méthode Buy lecteur Windows Media, classe externe
- Classe externe lecteur Windows Media, méthode Buy
topic_type:
- apiref
api_name:
- External.buy
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5ffee188372e33ed4ceadf1bb1ee2ea0f986207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545509"
---
# <a name="externalbuy-method"></a>External. Buy, méthode

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La méthode **Buy** lance l’achat d’un ensemble d’éléments multimédias.

## <a name="syntax"></a>Syntaxe


```JScript
External.buy(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ViewType* \[ dans\]
</dt> <dd>

**Chaîne** qui spécifie le type d’élément à acheter. L’appelant doit définir ce paramètre sur l’une des [constantes d’emplacement de bibliothèque](library-location-constants.md)suivantes :

CPListID

CPTrackID

CPAlbumID

</dd> <dt>

*ViewIDs* \[ dans\]
</dt> <dd>

**Chaîne** contenant les ID, délimités par des points-virgules, des éléments à acheter.

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

[**Objet externe pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. Download**](external-download.md)
</dt> <dt>

[**IWMPContentPartner :: Buy**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy)
</dt> <dt>

[**Achat de contenu multimédia**](purchasing-media-content.md)
</dt> </dl>

 

 





