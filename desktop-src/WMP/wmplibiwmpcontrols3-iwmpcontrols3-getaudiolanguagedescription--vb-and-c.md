---
title: Méthode IWMPControls3 getAudioLanguageDescription
description: La méthode getAudioLanguageDescription retourne la description de la langue audio correspondant à l’index de base 1 spécifié.
ms.assetid: bf3db27f-ba14-409e-8942-fe863d6f3670
keywords:
- méthode getAudioLanguageDescription lecteur Windows Media
- méthode getAudioLanguageDescription lecteur Windows Media, interface IWMPControls3
- Interface IWMPControls3 lecteur Windows Media, méthode getAudioLanguageDescription
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb45ceb166ca9c948823e516029569e457f35e27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537655"
---
# <a name="iwmpcontrols3getaudiolanguagedescription-method"></a>IWMPControls3 :: getAudioLanguageDescription, méthode

La méthode **getAudioLanguageDescription** retourne la description de la langue audio correspondant à l’index de base 1 spécifié.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String getAudioLanguageDescription(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageDescription( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPControls3.getAudioLanguageDescription
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*Lindex* \[ dans\]
</dt> <dd>

**System. Int32** qui est l’index de langage audio basé sur un.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**System. String** qui est la description de la langue audio.

## <a name="remarks"></a>Notes

Pour le contenu Windows Media, les propriétés et les méthodes liées à la sélection de la langue ne prennent en charge qu’une seule sortie.

Utilisez la propriété **audioLanguageCount** pour obtenir le nombre de langues audio prises en charge, puis accédez à une langue audio individuellement à l’aide d’un index de base un.

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

[**IWMPControls3. currentAudioLanguageIndex (VB et C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. currentAudioLanguage (VB et C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageID (VB et C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getLanguageName (VB et C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





