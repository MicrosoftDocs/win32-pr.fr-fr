---
title: DownloadCollection.id
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La propriété ID récupère l’ID de la collection de téléchargements.
ms.assetid: b5b17f22-913c-4055-8958-e3efac819b2b
keywords:
- DownloadCollection.id Lecteur Windows Media
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
ms.openlocfilehash: 97e505db2e643286f84b61bfa8604b9edc8ef36fa39cdd040bd9cc49bb98f82d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651268"
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

## <a name="remarks"></a>Remarques

Lorsque le gestionnaire de téléchargement crée une collection de téléchargements, il attribue un numéro d’identification au regroupement. les numéros d’identification sont conservés entre les sessions de Lecteur Windows Media et les sessions du système d’exploitation.

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

 

 





