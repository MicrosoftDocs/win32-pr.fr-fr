---
title: Controls. getAudioLanguageID, méthode
description: La méthode getAudioLanguageID récupère l’identificateur de paramètres régionaux (LCID) pour un index de langue audio spécifié.
ms.assetid: 8134a7ce-bdc7-46b2-b10e-2bf1215b0de1
keywords:
- Lecteur Windows Media de la méthode getAudioLanguageID
- méthode getAudioLanguageID Lecteur Windows Media, classe controls
- controls, classe Lecteur Windows Media, méthode getAudioLanguageID
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2352162d810ca75aeeee6db1c3d59c297b85414be46a365909c4ed56af179f8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119338"
---
# <a name="controlsgetaudiolanguageid-method"></a>Controls. getAudioLanguageID, méthode

La méthode **getAudioLanguageID** récupère l’identificateur de paramètres régionaux (LCID) pour un index de langue audio spécifié.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = Controls.getAudioLanguageID(
  index
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ dans\]
</dt> <dd>

**Nombre** (**long**) spécifiant l’index de langue audio.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un **nombre** (**long**).

## <a name="remarks"></a>Remarques

Un LCID identifie de façon unique un dialecte de langage particulier, appelé paramètres régionaux.

pour Windows le contenu multimédia, les propriétés et les méthodes liées à la sélection de la langue ne prennent en charge qu’une seule sortie.

**Lecteur Windows Media 10 Mobile :** Cette propriété retourne toujours le LCID de langue neutre (0).

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

[**Controls. currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls. getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls. getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





