---
title: Méthode IWMPControls3 getAudioLanguageID
description: La méthode getAudioLanguageID retourne l’identificateur de paramètres régionaux (LCID) pour un index de langue audio spécifié.
ms.assetid: 880bbfca-6f69-41ce-a078-467c1939fae5
keywords:
- Lecteur Windows Media de la méthode getAudioLanguageID
- méthode getAudioLanguageID Lecteur Windows Media, interface IWMPControls3
- Lecteur Windows Media de l’interface IWMPControls3, méthode getAudioLanguageID
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e853d5a13c40316341c0759899e06e7292c006c00068a1b527e5035ff10422b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506209"
---
# <a name="iwmpcontrols3getaudiolanguageid-method"></a>IWMPControls3 :: getAudioLanguageID, méthode

La méthode **getAudioLanguageID** retourne l’identificateur de paramètres régionaux (LCID) pour un index de langue audio spécifié.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 getAudioLanguageID(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageID( _
  ByVal lIndex As System.Int32 _
) As System.Int32
Implements IWMPControls3.getAudioLanguageID
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*Lindex* \[ dans\]
</dt> <dd>

**System. Int32** qui est l’index de base un de la langue audio.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**System. Int32** qui est le LCID.

## <a name="remarks"></a>Remarques

Un LCID identifie de façon unique un dialecte de langage particulier, appelé paramètres régionaux.

pour le contenu multimédia Windows, les propriétés et les méthodes associées à la sélection de la langue ne prennent en charge qu’une seule sortie.

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

[**IWMPControls3. currentAudioLanguage (VB et C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. currentAudioLanguageIndex (VB et C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageDescription (VB et C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getLanguageName (VB et C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





