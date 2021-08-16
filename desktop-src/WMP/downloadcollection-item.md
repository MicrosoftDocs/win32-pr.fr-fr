---
title: DownloadCollection. Item, méthode
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La méthode Item récupère un objet de téléchargement en attente.
ms.assetid: a79db9db-e80c-48db-aee6-9bd8f77a7dff
keywords:
- méthode item Lecteur Windows Media
- méthode item Lecteur Windows Media, classe DownloadCollection
- Lecteur Windows Media de la classe DownloadCollection, méthode item
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
ms.openlocfilehash: 8a82a903236038c2f0372786137eec48ad5c5f502d7fd614eb8944f3f4684aea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997038"
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

## <a name="remarks"></a>Remarques

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

 

 





