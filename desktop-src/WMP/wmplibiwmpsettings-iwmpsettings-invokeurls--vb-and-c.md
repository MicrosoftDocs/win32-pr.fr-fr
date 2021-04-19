---
title: IWMPSettings propriété invokeURLs
description: La propriété invokeURLs obtient ou définit une valeur indiquant si les événements d’URL doivent lancer un navigateur Web.
ms.assetid: e16c968d-a1b7-4c3a-9c1a-5748ed44cdac
keywords:
- propriété invokeURLs lecteur Windows Media
- propriété invokeURLs lecteur Windows Media, interface IWMPSettings
- Interface IWMPSettings lecteur Windows Media, propriété invokeURLs
topic_type:
- apiref
api_name:
- IWMPSettings.invokeURLs
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbdd68d797b54f4e9365f381b2b5c705dffc419b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530367"
---
# <a name="iwmpsettingsinvokeurls-property"></a>IWMPSettings :: invokeURLs, propriété

La propriété **invokeURLs** obtient ou définit une valeur indiquant si les événements d’URL doivent lancer un navigateur Web.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Boolean invokeURLs {get; set;}
```


```VB

Public Property invokeURLs As System.Boolean
```





## <a name="property-value"></a>Valeur de la propriété

Valeur **System. Boolean** indiquant si les événements d’URL doivent lancer un navigateur Web. La valeur par défaut est **true**.

## <a name="remarks"></a>Notes

Les fichiers multimédias numériques et les flux peuvent contenir des commandes de script d’URL. Lorsqu’une commande de script d’URL est envoyée au contrôle du lecteur Windows Media, elle est d’abord transmise au gestionnaire d’événements **\_ \_ ScriptCommandEvent AxWindowsMediaPlayer WMPOCXEvents** , quelle que soit la valeur récupérée par **invokeURLs**. Après la sortie de **\_ WMPOCXEvents \_ ScriptCommandEvent** , le lecteur Windows Media vérifie **invokeURLs** pour déterminer s’il faut lancer le navigateur Web par défaut avec l’URL. Vous pouvez afficher des URL de manière sélective en les vérifiant dans **\_ WMPOCXEvents \_ ScriptCommandEvent** et en définissant **invokeURLs** comme vous le souhaitez.

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

 

 





