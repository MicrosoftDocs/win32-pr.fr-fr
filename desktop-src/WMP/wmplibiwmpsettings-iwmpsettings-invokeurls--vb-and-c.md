---
title: IWMPSettings propriété invokeURLs
description: La propriété invokeURLs obtient ou définit une valeur indiquant si les événements d’URL doivent lancer un navigateur Web.
ms.assetid: e16c968d-a1b7-4c3a-9c1a-5748ed44cdac
keywords:
- Lecteur Windows Media de la propriété invokeURLs
- Lecteur Windows Media de la propriété invokeURLs, interface IWMPSettings
- Lecteur Windows Media de l’interface IWMPSettings, propriété invokeURLs
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
ms.openlocfilehash: dba44af7e6ec700f9df810486acb57af24a14c9e5d4966fddbfe4b242d346a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053427"
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

## <a name="remarks"></a>Remarques

Les fichiers multimédias numériques et les flux peuvent contenir des commandes de script d’URL. lorsqu’une commande de script d’URL est envoyée au contrôle Lecteur Windows Media, elle est passée en premier au gestionnaire d’événements **\_ \_ ScriptCommandEvent AxWindowsMediaPlayer WMPOCXEvents** , quelle que soit la valeur récupérée par **invokeURLs**. après la sortie de **\_ WMPOCXEvents \_ ScriptCommandEvent** , Lecteur Windows Media vérifie **invokeURLs** pour déterminer s’il faut lancer le navigateur Web par défaut avec l’URL. Vous pouvez afficher des URL de manière sélective en les vérifiant dans **\_ WMPOCXEvents \_ ScriptCommandEvent** et en définissant **invokeURLs** comme vous le souhaitez.

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

 

 





