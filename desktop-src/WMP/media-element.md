---
title: Élément multimédia
description: L’élément multimédia spécifie l’un des éléments multimédias dans une sélection.
ms.assetid: 7329bf48-3b23-4bc6-8488-506efca284bb
keywords:
- Élément multimédia lecteur Windows Media
topic_type:
- apiref
api_name:
- media Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e693c8b17345d3ba7875d48b83b5e3e90d682dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532698"
---
# <a name="media-element"></a>Élément multimédia

L’élément **multimédia** spécifie l’un des éléments multimédias dans une sélection.

``` syntax
<media
    src = "URL"
    cid = "WPL_GUID"
    tid = "WPL_GUID"
>
</media>
```

## <a name="attributes"></a>Attributs



| Terme                                                                                                                       | Description                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="src__required______________"></span><span id="SRC__REQUIRED______________"></span>**src** (obligatoire) <br/> | URL d’un élément multimédia.<br/>                                                              |
| <span id="cid"></span><span id="CID"></span>**confirmation**<br/>                                                             | ID de contenu qui est unique à cet élément multimédia.<br/>                                     |
| <span id="tid"></span><span id="TID"></span>**TID**<br/>                                                             | ID de suivi qui peut être utilisé pour effectuer le suivi de l’objet de système de fichiers pour cet élément multimédia.<br/> |



 

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy | Éléments               |
|-----------|------------------------|
| Parent    | [séquentiel](seq-element.md) |
| Enfant     | Aucune                   |



 

## <a name="remarks"></a>Notes

L’attribut **CID** (ID de contenu) est rempli par le lecteur Windows Media comme un moyen d’identifier de façon unique un morceau de contenu multimédia, même si ses attributs de métadonnées ont été modifiés. Cela permet de partager des sélections sur plusieurs ordinateurs, car le contenu peut être identifié sur un autre ordinateur, et le chemin d’accès peut être « réparé automatiquement » par la sélection Windows Media. L’attribut **TID** (l’ID de suivi) utilise le système de fichiers Windows pour réparer automatiquement le chemin d’accès au média si le nom ou l’emplacement du fichier est modifié.

## <a name="examples"></a>Exemples


```
<media
    src = "laure.wma"
    cid = "ABCDEFGH-abcd-1234-WXYZ-ABCDEF000000"
    tid = "12345678-1234-abcd-ABCD-123456abcDEF"
>
</media>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Seq, élément**](seq-element.md)
</dt> <dt>

[**Informations de référence sur les éléments de sélection Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





