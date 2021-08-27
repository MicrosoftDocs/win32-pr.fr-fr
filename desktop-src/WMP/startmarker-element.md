---
title: Élément STARTMARKER
description: l’élément STARTMARKER spécifie un marqueur à partir duquel Lecteur Windows Media démarrera le rendu du flux.
ms.assetid: b5c2422b-a59c-43f7-bac3-5722418192dc
keywords:
- élément STARTMARKER Lecteur Windows Media
topic_type:
- apiref
api_name:
- STARTMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2fa80da249edc4b9e3ab7d8796bc6ff135cb7cfb2b19a1cb11216ebe4a9c122c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123039"
---
# <a name="startmarker-element"></a>Élément STARTMARKER

l’élément **STARTMARKER** spécifie un marqueur à partir duquel Lecteur Windows Media démarrera le rendu du flux.

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
| Éléments enfants  | None               |



 

## <a name="remarks"></a>Remarques

cet élément spécifie le marqueur à partir duquel Lecteur Windows Media doit commencer à restituer le flux défini dans l' **entrée** parente ou l’élément **REF** .

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

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Référence du métafichier multimédia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





