---
title: Controls. currentAudioLanguageIndex
description: La propriété currentAudioLanguageIndex spécifie ou récupère l’index de base un qui correspond au langage audio pour la lecture.
ms.assetid: 9a1ae887-4e64-4758-a8a2-bf2e10a7a5c7
keywords:
- controls. currentAudioLanguageIndex Lecteur Windows Media
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguageIndex
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e783d42b957df40320b7c26814f7f05e93b94030518f45dc4b40d76f9ed32bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763869"
---
# <a name="controlscurrentaudiolanguageindex"></a>Controls. currentAudioLanguageIndex

La propriété **currentAudioLanguageIndex** spécifie ou récupère l’index de base un qui correspond au langage audio pour la lecture.

``` syntax
player.controls.currentAudioLanguageIndex
      
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture/écriture (**long**).

## <a name="remarks"></a>Remarques

pour Windows le contenu multimédia, les propriétés et les méthodes liées à la sélection de la langue ne prennent en charge qu’une seule sortie.

Utilisez la propriété **audioLanguageCount** pour connaître le nombre de langues audio prises en charge.

**Lecteur Windows Media 10 Mobile :** Cette propriété accepte ou retourne uniquement la valeur 0.

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

[**Controls. currentAudioLanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Controls. getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls. getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls. getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





