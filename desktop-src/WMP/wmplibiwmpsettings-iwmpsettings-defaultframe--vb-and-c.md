---
title: IWMPSettings propriété defaultFrame
description: La propriété defaultFrame obtient ou définit le nom du frame utilisé pour afficher une URL qui est reçue dans un \_ \_ événement ScriptCommandEvent WMPOCXEvents.
ms.assetid: 92c775ac-5ff1-4d21-b21d-491bc48a033f
keywords:
- Lecteur Windows Media de la propriété defaultFrame
- Lecteur Windows Media de la propriété defaultFrame, interface IWMPSettings
- Lecteur Windows Media de l’interface IWMPSettings, propriété defaultFrame
topic_type:
- apiref
api_name:
- IWMPSettings.defaultFrame
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39352b2c49bfdcd50f3e5c74d88a9fafef6752034dbd220cda3bb34dc0ed5de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053437"
---
# <a name="iwmpsettingsdefaultframe-property"></a>IWMPSettings ::d propriété efaultFrame

La propriété **defaultFrame** obtient ou définit le nom du frame utilisé pour afficher une URL qui est reçue dans un événement **\_ ScriptCommandEvent WMPOCXEvents \_** .

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String defaultFrame {get; set;}
```


```VB

Public Property defaultFrame As System.String
```





## <a name="property-value"></a>Valeur de la propriété

**System. String** qui est la valeur de l’attribut Name de l’élément **Frame** cible.

## <a name="remarks"></a>Remarques

Si un frame cible est spécifié dans l’événement **\_ WMPOCXEvents \_ ScriptCommandEvent** lui-même, cette propriété est ignorée.

Cette propriété est ignorée lors de l’utilisation de l’applet Java de Netscape Navigator. Dans Netscape Navigator, chaque commande de script d’URL reçue affiche l’URL dans une nouvelle fenêtre de navigateur, quelle que soit la valeur de **defaultFrame**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**événement AxWindowsMediaPlayer. commande (VB et C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**Interface IWMPSettings (VB et C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





