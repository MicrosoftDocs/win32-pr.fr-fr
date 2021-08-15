---
title: Élément multimédia
description: L’élément multimédia spécifie l’un des éléments multimédias dans une sélection.
ms.assetid: 7329bf48-3b23-4bc6-8488-506efca284bb
keywords:
- élément multimédia Lecteur Windows Media
topic_type:
- apiref
api_name:
- media Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c67f4321d85ec52babbc6f24c2cd9e3512f7c970eb3360ba2ddfd7ba53f82152
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996319"
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
| Enfant     | None                   |



 

## <a name="remarks"></a>Remarques

l’attribut **cid** (ID de contenu) est rempli par le Lecteur Windows Media comme un moyen d’identifier de façon unique un morceau de contenu multimédia, même si ses attributs de métadonnées ont été modifiés. cela permet de partager des sélections sur plusieurs ordinateurs, car le contenu peut être identifié sur un autre ordinateur, et le chemin d’accès peut être « réparé automatiquement » par la sélection de média Windows. l’attribut **tid** (l’ID de suivi) utilise le système de fichiers Windows pour réparer automatiquement le chemin d’accès au média si le nom ou l’emplacement du fichier est modifié.

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

[**Windows Référence des éléments de sélection de média**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





