---
title: Controls. getLanguageName, méthode
description: La méthode getLanguageName récupère le nom de la langue audio avec l’identificateur de paramètres régionaux (LCID) spécifié.
ms.assetid: 9e142c89-92bf-476f-bae7-b94f5b5ebe01
keywords:
- Lecteur Windows Media de la méthode getLanguageName
- méthode getLanguageName Lecteur Windows Media, classe controls
- controls, classe Lecteur Windows Media, méthode getLanguageName
topic_type:
- apiref
api_name:
- Controls.getLanguageName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 798a6b22f344953df716e4df4ed8a9a0daff2a7b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919352"
---
# <a name="controlsgetlanguagename-method"></a>Controls. getLanguageName, méthode

La méthode **getLanguageName** récupère le nom de la langue audio avec l’identificateur de paramètres régionaux (LCID) spécifié.

## <a name="syntax"></a>Syntaxe


```JScript
strRetVal = Controls.getLanguageName(
  LCID
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*LCID* \[ dans\]
</dt> <dd>

**Nombre** (**long**) spécifiant le LCID.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne une **chaîne**.

## <a name="remarks"></a>Notes

Un LCID identifie de façon unique un dialecte de langage particulier, appelé paramètres régionaux.

pour Windows le contenu multimédia, les propriétés et les méthodes liées à la sélection de la langue ne prennent en charge qu’une seule sortie.

## <a name="requirements"></a>Spécifications



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

[**Controls. getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> </dl>

 

 





