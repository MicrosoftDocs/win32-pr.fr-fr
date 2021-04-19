---
title: PLAYLIST. itemPlaylist
description: L’attribut itemPlaylist récupère la sélection de l’élément multimédia qui est affiché à l’index donné dans l’élément PLAYLIST.
ms.assetid: 094bcb5d-8a59-4531-96b8-0e993ca00be6
keywords:
- Lecteur Windows Media PLAYLIST. itemPlaylist
topic_type:
- apiref
api_name:
- PLAYLIST.itemPlaylist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d414692050e16dfd0aebe05901bcee0bc26580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543323"
---
# <a name="playlistitemplaylist"></a>PLAYLIST. itemPlaylist

L’attribut **itemPlaylist** récupère la sélection de l’élément multimédia qui est affiché à l’index donné dans l’élément **playlist** .

``` syntax
        elementID.itemPlaylist(index)
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un objet de **sélection** en lecture seule.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*évaluer*
</dt> <dd>

**Nombre**(**long**) contenant l’index d’un élément de sélection.

</dd> </dl>

## <a name="remarks"></a>Notes

La propriété **itemPlaylist** retourne l’objet playlist qui est développé dans l’élément **playlist** . Par exemple, s’il existe deux sélections imbriquées qui ne sont pas développées dans l’élément **playlist** et qui contiennent trois clips multimédias, **itemPlaylist**(1) retourne la sélection parente qui contient les deux sélections imbriquées. Si la deuxième sélection est développée, **itemPlaylist**(1) retourne la deuxième sélection. Si les deux sélections sont développées, **itemPlaylist**(1) retourne la première sélection.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> <dt>

[**Objet playlist**](playlist-object.md)
</dt> </dl>

 

 





