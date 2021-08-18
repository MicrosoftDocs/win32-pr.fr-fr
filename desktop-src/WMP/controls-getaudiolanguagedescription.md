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
ms.openlocfilehash: 29aa5f7b5c0ad72ff13b571505283b243bd62d79ebc4339717ed8283cccb2a5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997499"
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

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne une valeur de **chaîne** .

## <a name="remarks"></a>Remarques

pour Windows le contenu multimédia, les propriétés et les méthodes liées à la sélection de la langue ne prennent en charge qu’une seule sortie.

Utilisez la propriété **audioLanguageCount** pour obtenir le nombre de langues audio prises en charge, puis accédez à une langue audio individuellement à l’aide d’un index de base un.

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.

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

[**Controls. getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls. getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





