---
title: DownloadItem.downloadState
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La propriété downloadState récupère l’état du téléchargement.
ms.assetid: dde27f43-40ee-4eb9-b316-42312ee937d0
keywords:
- DownloadItem. downloadState Lecteur Windows Media
topic_type:
- apiref
api_name:
- DownloadItem.downloadState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f2f1d7338370aaa5132c479d155ffbfc4282a686d082df37446be053efab3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997049"
---
# <a name="downloaditemdownloadstate"></a>DownloadItem.downloadState

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La propriété **downloadState** récupère l’état du téléchargement.

## <a name="syntax"></a>Syntaxe

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).downloadState
      
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule contenant l’une des valeurs suivantes.



| Valeur | Description |
|-------|-------------|
| 0     | Downloading |
| 1     | Suspendu      |
| 2     | Traitement en cours  |
| 3     | Effectué   |
| 4     | Opération annulée    |



 

## <a name="remarks"></a>Remarques

Les États de téléchargement peuvent se produire dans n’importe quel ordre. N’écrivez pas de code qui dépend de l’occurrence d’un état de téléchargement particulier.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





