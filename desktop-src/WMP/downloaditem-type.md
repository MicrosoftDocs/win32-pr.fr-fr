---
title: DownloadItem. type
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La propriété type récupère le type du téléchargement.
ms.assetid: 58ffb8a3-5410-492b-bb0f-9130ed209b78
keywords:
- DownloadItem. type lecteur Windows Media
topic_type:
- apiref
api_name:
- DownloadItem.type
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cdcf21ce7443d7730d4a75518fb4749af0b9e52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526011"
---
# <a name="downloaditemtype"></a>DownloadItem. type

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La propriété **type** récupère le type du téléchargement.

## <a name="syntax"></a>Syntaxe

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).type
      
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture seule qui contient l’une des valeurs suivantes.



| Valeur      | Description                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| background | (Windows XP uniquement.) Le téléchargement se produit en tant que processus en arrière-plan, car le temps processeur devient disponible. Les États de téléchargement persistent même lorsque Windows Media Player ou Windows XP est arrêté. |
| temps réel  | (Tous les systèmes d’exploitation pris en charge.) Le téléchargement a lieu en même temps. Aucun État de téléchargement n’est conservé entre les sessions.                                                                       |



 

## <a name="remarks"></a>Notes

Chaque type de téléchargement présente des avantages et des inconvénients. Le téléchargement en arrière-plan permet à l’utilisateur de passer à d’autres tâches et même de redémarrer Windows sans annuler le téléchargement, mais prend plus de temps pour effectuer le téléchargement et n’est pris en charge que pour Windows XP. Le téléchargement en temps réel prend moins de temps, mais exige que l’utilisateur termine tout téléchargement avant de fermer le lecteur Windows Media.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





