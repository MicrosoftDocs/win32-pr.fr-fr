---
title: Méthode IWMPControls3 getLanguageName
description: La méthode getLanguageName retourne le nom de la langue audio avec l’identificateur de paramètres régionaux (LCID) spécifié.
ms.assetid: a0651e8d-0ba1-4fff-93f0-fe097231723e
keywords:
- Lecteur Windows Media de la méthode getLanguageName
- méthode getLanguageName Lecteur Windows Media, interface IWMPControls3
- Lecteur Windows Media de l’interface IWMPControls3, méthode getLanguageName
topic_type:
- apiref
api_name:
- IWMPControls3.getLanguageName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6850bd73c9add044bdb845d17341745c7546918f7824b611ed2f018f66139d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000489"
---
# <a name="iwmpcontrols3getlanguagename-method"></a>IWMPControls3 :: getLanguageName, méthode

La méthode **getLanguageName** retourne le nom de la langue audio avec l’identificateur de paramètres régionaux (LCID) spécifié.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String getLanguageName(
  System.Int32 lLangID
);
```


```VB

Public Function getLanguageName( _
  ByVal lLangID As System.Int32 _
) As System.String
Implements IWMPControls3.getLanguageName
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*lLangID* \[ dans\]
</dt> <dd>

**System. Int32** qui est le LCID.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**System. String** qui est le nom de la langue audio.

## <a name="remarks"></a>Remarques

Un LCID identifie de façon unique un dialecte de langage particulier, appelé paramètres régionaux.

pour Windows le contenu multimédia, les propriétés et les méthodes liées à la sélection de la langue prennent en charge une seule sortie.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPControls3 (VB et C#)**](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. audioLanguageCount (VB et C#)**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. currentAudioLanguage (VB et C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. currentAudioLanguageIndex (VB et C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageDescription (VB et C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageID (VB et C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> </dl>

 

 





