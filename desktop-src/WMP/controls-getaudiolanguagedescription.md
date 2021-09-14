---
title: Controls. getAudioLanguageDescription, méthode
description: La méthode getAudioLanguageDescription récupère la description de la langue audio correspondant à l’index de base 1 spécifié.
ms.assetid: 995a2568-f15f-4b92-9782-92ba5273f444
keywords:
- Lecteur Windows Media de la méthode getAudioLanguageDescription
- méthode getAudioLanguageDescription Lecteur Windows Media, classe controls
- controls, classe Lecteur Windows Media, méthode getAudioLanguageDescription
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageDescription
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d28e82648a1047252402694f4948d2a2734f344
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919351"
---
# <a name="controlsgetaudiolanguagedescription-method"></a>Controls. getAudioLanguageDescription, méthode

La méthode **getAudioLanguageDescription** récupère la description de la langue audio correspondant à l’index de base 1 spécifié.

## <a name="syntax"></a>Syntaxe


```JScript
strRetVal = Controls.getAudioLanguageDescription(
  index
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ dans\]
</dt> <dd>

**Nombre** (**long**) spécifiant l’index de langue audio basé sur un.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne une valeur de **chaîne** .

## <a name="remarks"></a>Notes

pour Windows le contenu multimédia, les propriétés et les méthodes liées à la sélection de la langue ne prennent en charge qu’une seule sortie.

Utilisez la propriété **audioLanguageCount** pour obtenir le nombre de langues audio prises en charge, puis accédez à une langue audio individuellement à l’aide d’un index de base un.

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.

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

[**Controls. getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls. getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





