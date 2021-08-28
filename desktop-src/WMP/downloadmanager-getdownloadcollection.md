---
title: Méthode DownloadManager. getDownloadCollection
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La méthode getDownloadCollection récupère la collection de téléchargements spécifiée.
ms.assetid: 743d6bcf-2d5b-4a30-a4ef-4538cf7c901e
keywords:
- Lecteur Windows Media de la méthode getDownloadCollection
- méthode getDownloadCollection Lecteur Windows Media, classe DownloadManager
- Lecteur Windows Media de la classe DownloadManager, méthode getDownloadCollection
topic_type:
- apiref
api_name:
- DownloadManager.getDownloadCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57fc729296f15b39e603683cab38e3d0d878733ab0990d9876e32b4001a15cf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749619"
---
# <a name="downloadmanagergetdownloadcollection-method"></a>Méthode DownloadManager. getDownloadCollection

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La méthode **getDownloadCollection** récupère la collection de téléchargements spécifiée.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = DownloadManager.getDownloadCollection(
  collectionId
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

L’un des  \[ dans\]
</dt> <dd>

**Nombre** (**long**) spécifiant l’ID de la collection de téléchargements à récupérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un objet **DownloadCollection** .

## <a name="remarks"></a>Remarques

Vous devez d’abord appeler *downloadmanager*. **createDownloadCollection** pour créer une nouvelle collection et récupérer sa valeur d’ID.

Une collection de téléchargements existante peut contenir des éléments qui ont été marqués comme étant annulés.

Les éléments de téléchargement en temps réel qui ne sont pas terminés dans une session antérieure ne sont pas récupérés dans le cadre de la collection. Les téléchargements en arrière-plan qui ont été effectués avant la session active restent dans la collection de téléchargements jusqu’à ce qu’ils soient supprimés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DownloadManager**](downloadmanager-object.md)
</dt> <dt>

[**DownloadManager. createDownloadCollection**](downloadmanager-createdownloadcollection.md)
</dt> <dt>

[**Objet DownloadCollection**](downloadcollection-object.md)
</dt> </dl>

 

 





