---
title: DownloadCollection.id
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La propriété ID récupère l’ID de la collection de téléchargements.
ms.assetid: b5b17f22-913c-4055-8958-e3efac819b2b
keywords:
- Lecteur Windows Media DownloadCollection.id
topic_type:
- apiref
api_name:
- DownloadCollection.id
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9edcca4f56c485951ca907ae228dfec7a958b308
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541764"
---
# <a name="downloadcollectionid"></a>DownloadCollection.id

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La propriété **ID** récupère l’ID de la collection de téléchargements.

## <a name="syntax"></a>Syntaxe

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).id
      
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**).

## <a name="remarks"></a>Notes

Lorsque le gestionnaire de téléchargement crée une collection de téléchargements, il attribue un numéro d’identification au regroupement. Les numéros d’identification sont conservés entre les sessions du lecteur Windows Media et les sessions du système d’exploitation.

Les numéros d’ID ne sont pas uniques. Toutefois, il existe un nombre suffisant de numéros d’ID disponibles dans la valeur 32 bits, car il est très improbable qu’un numéro d’identification existant soit remplacé par un nouveau.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DownloadCollection**](downloadcollection-object.md)
</dt> </dl>

 

 





