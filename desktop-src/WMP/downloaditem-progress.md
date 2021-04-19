---
title: DownloadItem. Progress
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La propriété Progress récupère la progression du téléchargement en octets.
ms.assetid: 58644eac-8dd0-4e9d-8055-03833c863a6e
keywords:
- DownloadItem. Progress lecteur Windows Media
topic_type:
- apiref
api_name:
- DownloadItem.progress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a1967c1eb3dc72c00b8b10b70da5d797343e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535919"
---
# <a name="downloaditemprogress"></a>DownloadItem. Progress

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La propriété **Progress** récupère la progression du téléchargement en octets.

## <a name="syntax"></a>Syntaxe

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).progress
      
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DownloadItem**](downloaditem-object.md)
</dt> <dt>

[**DownloadItem. Size**](downloaditem-size.md)
</dt> </dl>

 

 





