---
title: DownloadCollection. removeItem, méthode
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La méthode removeItem supprime un élément de téléchargement d’une collection de téléchargements.
ms.assetid: 0008752e-c81a-4f91-a582-9d6b46569479
keywords:
- méthode removeItem lecteur Windows Media
- méthode removeItem lecteur Windows Media, classe DownloadCollection
- Classe DownloadCollection lecteur Windows Media, removeItem, méthode
topic_type:
- apiref
api_name:
- DownloadCollection.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1798665b79327b7956c1b78509b55cc6e6dd70c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543962"
---
# <a name="downloadcollectionremoveitem-method"></a>DownloadCollection. removeItem, méthode

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La méthode **RemoveItem** supprime un élément de téléchargement d’une collection de téléchargements.

## <a name="syntax"></a>Syntaxe


```JScript
DownloadCollection.removeItem(
  itemID
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ItemId* \[ dans\]
</dt> <dd>

**Nombre** (**long**) spécifiant l’index du **DownloadItem** à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si le téléchargement représenté par *ItemId* est en cours, cette méthode annule le téléchargement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DownloadCollection. Item**](downloadcollection-item.md)
</dt> <dt>

[**Objet DownloadCollection**](downloadcollection-object.md)
</dt> </dl>

 

 





