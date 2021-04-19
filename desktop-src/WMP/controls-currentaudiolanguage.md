---
title: Controls. currentAudioLanguage
description: La propriété currentAudioLanguage spécifie ou récupère l’identificateur de paramètres régionaux (LCID) de la langue audio pour la lecture.
ms.assetid: 628845df-add3-4068-9c3d-b4a9b818808c
keywords:
- Controls. currentAudioLanguage Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguage
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1bc84c7d4c14bb742a6db37feca59fb9d0db0e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537566"
---
# <a name="controlscurrentaudiolanguage"></a>Controls. currentAudioLanguage

La propriété **currentAudioLanguage** spécifie ou récupère l’identificateur de paramètres régionaux (LCID) de la langue audio pour la lecture.

``` syntax
player.controls.currentAudioLanguage
      
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture/écriture (**long**).

## <a name="remarks"></a>Notes

Un LCID identifie de façon unique un dialecte de langage particulier, appelé paramètres régionaux.

Pour le contenu Windows Media, les propriétés et les méthodes liées à la sélection de la langue ne prennent en charge qu’une seule sortie.

Lors de l’utilisation d’un contenu DVD, la spécification d’un LCID entraîne la sélection de la première piste audio disponible avec l’ID de langue spécifié.

**Lecteur Windows Media 10 Mobile :** Cette propriété accepte ou retourne uniquement le LCID de langue neutre (0).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Controls (objet)**](controls-object.md)
</dt> <dt>

[**Controls. audioLanguageCount**](controls-audiolanguagecount.md)
</dt> <dt>

[**Controls. currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls. getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls. getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls. getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





