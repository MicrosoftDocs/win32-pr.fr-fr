---
title: DownloadItem.sourceURL
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La propriété sourceURL récupère l’URL source du téléchargement.
ms.assetid: 87af20a5-5721-498d-8417-3e7dbbec38a2
keywords:
- Lecteur Windows Media DownloadItem. sourceURL
topic_type:
- apiref
api_name:
- DownloadItem.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1670fb4fec0ff4adb68269cf6fe6bb39be248e01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525441"
---
# <a name="downloaditemsourceurl"></a>DownloadItem.sourceURL

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La propriété **sourceURL** récupère l’URL source du téléchargement.

## <a name="syntax"></a>Syntaxe

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).sourceURL
      
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture seule.

## <a name="remarks"></a>Notes

Seuls les formats multimédias numériques suivants peuvent être téléchargés :

-   ASF (Advanced Systems Format)
-   MP3
-   Audio Windows Media (WMA)
-   Vidéo Windows Media (WMV)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





