---
description: Contient un objet qui représente une application.
ms.assetid: 61B85691-399D-41c1-9901-825345A38E5A
title: IShellDispatch. application, propriété (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5fbdbd8b2cc847a1b06a316d6f8caebfe1e2e5e4fc79fc4be2ff2ebdb8ee3912
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119443319"
---
# <a name="ishelldispatchapplication-property"></a>IShellDispatch. application, propriété

Contient un objet qui représente une application.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
objApplication = IShellDispatch.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a>Valeur de la propriété

Variable de type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui reçoit l’objet application.

## <a name="remarks"></a>Remarques

Cette propriété est implémentée et accessible via la propriété [**Shell. EjectPC**](shell-ejectpc.md) .

La propriété d' **application** retourne l’objet Automation pris en charge par l’application qui contient le contrôle WebBrowser, si cet objet est accessible. Sinon, cette propriété retourne l’objet Automation du contrôle WebBrowser.

utilisez cette propriété avec les commandes **Set** et **CreateObject** ou à l’aide de la commande **GetObject** pour créer et manipuler une instance du Windows application Internet Explorer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 
