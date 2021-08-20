---
title: External. Download, méthode
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La méthode Download lance le téléchargement d’un ensemble d’éléments multimédias.
ms.assetid: 10bae41c-0658-4712-8a7e-375a1ec6dc25
keywords:
- télécharger la méthode Lecteur Windows Media
- télécharger la méthode Lecteur Windows Media, classe externe
- Lecteur Windows Media de classe externe, méthode de téléchargement
topic_type:
- apiref
api_name:
- External.download
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 766f96a6db5f2114724e7545eaac7a269bf52e2e657872a8078b490621c794df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649219"
---
# <a name="externaldownload-method"></a>External. Download, méthode

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La méthode **Download** lance le téléchargement d’un ensemble d’éléments multimédias.

## <a name="syntax"></a>Syntaxe


```JScript
External.download(
  Type,
  IDs
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Type* \[ dans\]
</dt> <dd>

[Constante d’emplacement de bibliothèque](library-location-constants.md) qui spécifie le type d’élément à télécharger. Par exemple, CPTrackID spécifie qu’une ou plusieurs pistes doivent être téléchargées.

</dd> <dt>

*ID* \[ dans\]
</dt> <dd>

**Chaîne** contenant les ID, délimités par des points-virgules, des éléments multimédias à télécharger.

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

[**Téléchargement du contenu multimédia**](downloading-media-content.md)
</dt> <dt>

[**Objet externe pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Externe. acheter**](external-buy.md)
</dt> <dt>

[**IWMPContentPartner ::D lécharger**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)
</dt> </dl>

 

 





