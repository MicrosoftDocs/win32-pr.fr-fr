---
title: Élément STARTMARKER
description: L’élément STARTMARKER spécifie un marqueur à partir duquel le lecteur Windows Media va commencer le rendu du flux.
ms.assetid: b5c2422b-a59c-43f7-bac3-5722418192dc
keywords:
- Élément STARTMARKER lecteur Windows Media
topic_type:
- apiref
api_name:
- STARTMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c3b3afbc3ab4a922d17f6a0269ed89c22f4dfeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535340"
---
# <a name="startmarker-element"></a>Élément STARTMARKER

L’élément **STARTMARKER** spécifie un marqueur à partir duquel le lecteur Windows Media va commencer le rendu du flux.

``` syntax
<STARTMARKER
   NUMBER = "marker number"
   NAME = "marker name"
/>
```

## <a name="attributes"></a>Attributs

**CERTAIN**

Numéro d’un marqueur numérique dans l’index. La valeur par défaut est le début du contenu à la demande ou la position actuelle dans un flux en temps réel.

**NAME**

Nom d’un marqueur nommé dans l’index. La valeur par défaut est le début du contenu à la demande ou la position actuelle dans un flux en temps réel.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments           |
|-----------------|--------------------|
| Éléments parents | **entry**, **ref** |
| Éléments enfants  | Aucune               |



 

## <a name="remarks"></a>Notes

Cet élément spécifie le marqueur à partir duquel le lecteur Windows Media doit commencer le rendu du flux défini dans l' **entrée** parente ou l’élément **ref** .

**Remarque**

Utilisez cet élément avec l’attribut **Number** ou **Name** , mais pas les deux.

Un élément **STARTMARKER** défini dans un élément **ref** est prioritaire sur un élément **STARTMARKER** défini dans l’élément d' **entrée** parent de l’élément **ref** . Un élément **STARTMARKER** est également prioritaire sur un élément **StartTime** .

Si le marqueur spécifié par un élément **STARTMARKER** se produit plus tard dans le flux que le marqueur défini par un élément **ENDMARKER** , aucun contenu n’est lu, mais aucune erreur n’est générée.

## <a name="examples"></a>Exemples


```XML
<STARTMARKER NUMBER="14" />
<STARTMARKER NAME="Marker_StartHere" />
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 70 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Informations de référence sur les éléments de métafichier Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informations de référence sur les métafichiers Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





