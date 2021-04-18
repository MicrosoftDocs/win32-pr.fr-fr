---
title: DownloadCollection. Item, méthode
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La méthode Item récupère un objet de téléchargement en attente.
ms.assetid: a79db9db-e80c-48db-aee6-9bd8f77a7dff
keywords:
- méthode Item lecteur Windows Media
- méthode Item lecteur Windows Media, classe DownloadCollection
- Classe DownloadCollection lecteur Windows Media, méthode Item
topic_type:
- apiref
api_name:
- DownloadCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57db60a776c71d9ff16eceb1584c79a125bbf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526816"
---
# <a name="downloadcollectionitem-method"></a>DownloadCollection. Item, méthode

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La méthode **Item** récupère un objet de téléchargement en attente.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = DownloadCollection.item(
  itemId
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ItemId* \[ dans\]
</dt> <dd>

**Nombre** (**long**) spécifiant l’index du **DownloadItem** à récupérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un objet **DownloadItem** .

## <a name="remarks"></a>Notes

La valeur *ItemId* est de base zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DownloadCollection**](downloadcollection-object.md)
</dt> <dt>

[**Objet DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





