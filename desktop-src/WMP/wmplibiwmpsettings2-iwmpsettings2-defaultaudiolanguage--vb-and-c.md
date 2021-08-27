---
title: IWMPSettings2 propriété defaultAudioLanguage
description: la propriété defaultAudioLanguage obtient l’identificateur de paramètres régionaux (LCID) de la langue audio par défaut spécifiée dans Lecteur Windows Media.
ms.assetid: 4b7c9639-9d9f-4ed7-bb70-12cc608dd57a
keywords:
- Lecteur Windows Media de la propriété defaultAudioLanguage
- Lecteur Windows Media de la propriété defaultAudioLanguage, interface IWMPSettings2
- Lecteur Windows Media de l’interface IWMPSettings2, propriété defaultAudioLanguage
topic_type:
- apiref
api_name:
- IWMPSettings2.defaultAudioLanguage
- IWMPSettings2.get_defaultAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f09df11cc53e9b813de2e40e40eca1e31a88afeff0c16ce1f9c0c5ba4745277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331099"
---
# <a name="iwmpsettings2defaultaudiolanguage-property"></a>IWMPSettings2 ::d propriété efaultAudioLanguage

la propriété **defaultAudioLanguage** obtient l’identificateur de paramètres régionaux (LCID) de la langue audio par défaut spécifiée dans Lecteur Windows Media.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 defaultAudioLanguage {get;}
```


```VB

Public ReadOnly Property defaultAudioLanguage As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui est le LCID.

## <a name="remarks"></a>Remarques

Un LCID identifie de façon unique un dialecte de langage particulier, appelé paramètres régionaux.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWMPControls3. currentAudioLanguage (VB et C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**Interface IWMPSettings (VB et C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Interface IWMPSettings2 (VB et C#)**](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





