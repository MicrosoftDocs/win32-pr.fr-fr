---
title: Méthode IMsTscAxEvents OnRemoteWindowDisplayed
description: Appelé lorsqu’une fenêtre RemoteApp est affichée.
ms.assetid: B1E83486-50CB-4CA4-BD01-2C72938335AF
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnRemoteWindowDisplayed
- Méthode OnRemoteWindowDisplayed Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnRemoteWindowDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteWindowDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f03029f31e1ce2133c74c92c0d6d57f192e4d85f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384880"
---
# <a name="imstscaxeventsonremotewindowdisplayed-method"></a>IMsTscAxEvents :: OnRemoteWindowDisplayed, méthode

Appelé lorsqu’une fenêtre RemoteApp est affichée.

## <a name="syntax"></a>Syntaxe


```C++
void OnRemoteWindowDisplayed(
  [in] VARIANT_BOOL                   vbDisplayed,
  [in] HWND                           hwnd,
  [in] RemoteWindowDisplayedAttribute windowAttribute
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*vbDisplayed* \[ dans\]
</dt> <dd>

Type : **Variant \_ bool**

Indique si la fenêtre RemoteApp est affichée ou masquée.

</dd> <dt>

*HWND* \[ dans\]
</dt> <dd>

Type : **HWND**

Handle de la fenêtre affichée.

</dd> <dt>

*windowAttribute* \[ dans\]
</dt> <dd>

Type : **[ **RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)**

Valeur de l’énumération [**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md) qui spécifie plus d’informations sur l’événement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)
</dt> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





