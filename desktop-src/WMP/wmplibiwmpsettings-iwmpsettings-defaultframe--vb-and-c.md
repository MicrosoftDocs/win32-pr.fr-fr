---
title: IWMPSettings propriété defaultFrame
description: La propriété defaultFrame obtient ou définit le nom du frame utilisé pour afficher une URL qui est reçue dans un \_ \_ événement ScriptCommandEvent WMPOCXEvents.
ms.assetid: 92c775ac-5ff1-4d21-b21d-491bc48a033f
keywords:
- propriété defaultFrame lecteur Windows Media
- propriété defaultFrame lecteur Windows Media, interface IWMPSettings
- Interface IWMPSettings lecteur Windows Media, propriété defaultFrame
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
ms.openlocfilehash: 28539640214165ab5b2808762ed854b19b434311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525398"
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

## <a name="remarks"></a>Notes

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

[**Événement AxWindowsMediaPlayer. commande (VB et C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**Interface IWMPSettings (VB et C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





