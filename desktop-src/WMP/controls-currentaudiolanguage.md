---
title: Controls. currentAudioLanguage
description: La propriété currentAudioLanguage spécifie ou récupère l’identificateur de paramètres régionaux (LCID) de la langue audio pour la lecture.
ms.assetid: 628845df-add3-4068-9c3d-b4a9b818808c
keywords:
- controls. currentAudioLanguage Lecteur Windows Media
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
ms.openlocfilehash: 63c5eb53c9f408a9d50a7f738434e5dcd30fc804970b3e1ea95c985c90d62063
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750611"
---
# <a name="controlscurrentaudiolanguage"></a>Controls. currentAudioLanguage

La propriété **currentAudioLanguage** spécifie ou récupère l’identificateur de paramètres régionaux (LCID) de la langue audio pour la lecture.

``` syntax
player.controls.currentAudioLanguage
      
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture/écriture (**long**).

## <a name="remarks"></a>Remarques

Un LCID identifie de façon unique un dialecte de langage particulier, appelé paramètres régionaux.

pour Windows le contenu multimédia, les propriétés et les méthodes liées à la sélection de la langue ne prennent en charge qu’une seule sortie.

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

 

 





