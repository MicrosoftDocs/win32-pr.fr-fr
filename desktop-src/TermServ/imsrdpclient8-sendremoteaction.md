---
title: Méthode IMsRdpClient8 SendRemoteAction
description: Entraîne l’exécution d’une action dans la session à distance.
ms.assetid: d6a43662-7e51-404a-a3f9-a8b51cbc69d1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SendRemoteAction
- Méthode SendRemoteAction Services Bureau à distance, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, méthode SendRemoteAction
- Méthode SendRemoteAction Services Bureau à distance, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, méthode SendRemoteAction
- Méthode SendRemoteAction Services Bureau à distance, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, méthode SendRemoteAction
topic_type:
- apiref
api_name:
- IMsRdpClient8.SendRemoteAction
- IMsRdpClient9.SendRemoteAction
- IMsRdpClient10.SendRemoteAction
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a28fc9695686402e0a8e98ed17fc1bc6a47939d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467031"
---
# <a name="imsrdpclient8sendremoteaction-method"></a>IMsRdpClient8 :: SendRemoteAction, méthode

Entraîne l’exécution d’une action dans la session à distance.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SendRemoteAction(
  [in] RemoteSessionActionType actionType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ActionType* \[ dans\]
</dt> <dd>

Valeur de l’énumération [**RemoteSessionActionType**](remotesessionactiontype.md) qui spécifie l’action à envoyer à la session à distance.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient8 est défini en tant que 4247E044-9271-43A9-BC49-E2AD9E855D62<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





