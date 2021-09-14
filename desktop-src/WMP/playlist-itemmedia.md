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
ms.openlocfilehash: 269e9011ade69ee61d99c29c1fa5bd1b9fa3deeb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193204"
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

## <a name="remarks"></a>Notes

La propriété **itemMedia** retourne des objets multimédias qui sont développés dans l’élément **playlist** . Par exemple, s’il existe une sélection qui contient trois clips multimédias qui ne sont pas développés dans l’élément **playlist** , **itemMedia**(0) retourne la playlist en tant qu’objet multimédia. Si la sélection est développée, **itemMedia**(0) retourne le premier clip multimédia de la sélection.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Media**](media-object.md)
</dt> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





