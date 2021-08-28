---
title: PLAYLIST. itemMedia
description: L’attribut itemMedia récupère l’objet Media correspondant à l’index donné dans l’élément PLAYLIST.
ms.assetid: 38085798-7986-432f-8c88-de886bfc2ac5
keywords:
- PLAYLIST. itemMedia Lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.itemMedia
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52b3061ef83ec246878d51528e88a12b4f10dcb3085f584a2266dc64a163b866
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746864"
---
# <a name="playlistitemmedia"></a>PLAYLIST. itemMedia

L’attribut **itemMedia** récupère l’objet **Media** correspondant à l’index donné dans l’élément **playlist** .

``` syntax
        elementID.itemMedia(index)
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un objet **multimédia** en lecture seule.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*évaluer*
</dt> <dd>

**Nombre**(**long**) contenant l’index d’un élément de sélection.

</dd> </dl>

## <a name="remarks"></a>Remarques

La propriété **itemMedia** retourne des objets multimédias qui sont développés dans l’élément **playlist** . Par exemple, s’il existe une sélection qui contient trois clips multimédias qui ne sont pas développés dans l’élément **playlist** , **itemMedia**(0) retourne la playlist en tant qu’objet multimédia. Si la sélection est développée, **itemMedia**(0) retourne le premier clip multimédia de la sélection.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Media**](media-object.md)
</dt> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





