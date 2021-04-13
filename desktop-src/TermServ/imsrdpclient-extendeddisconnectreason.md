---
title: IMsRdpClient propriété ExtendedDisconnectReason
description: Contient des informations étendues sur la raison de la déconnexion du contrôle.
ms.assetid: 5729992f-6695-44c0-8cf0-0d6b4cbddb62
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ExtendedDisconnectReason
- Services Bureau à distance de la propriété ExtendedDisconnectReason, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété ExtendedDisconnectReason
- Services Bureau à distance de la propriété ExtendedDisconnectReason, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété ExtendedDisconnectReason
- Services Bureau à distance de la propriété ExtendedDisconnectReason, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété ExtendedDisconnectReason
- Services Bureau à distance de la propriété ExtendedDisconnectReason, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété ExtendedDisconnectReason
- Services Bureau à distance de la propriété ExtendedDisconnectReason, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété ExtendedDisconnectReason
- Services Bureau à distance de la propriété ExtendedDisconnectReason, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété ExtendedDisconnectReason
- Services Bureau à distance de la propriété ExtendedDisconnectReason, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété ExtendedDisconnectReason
- Services Bureau à distance de la propriété ExtendedDisconnectReason, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété ExtendedDisconnectReason
- Services Bureau à distance de la propriété ExtendedDisconnectReason, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété ExtendedDisconnectReason
- Services Bureau à distance de la propriété ExtendedDisconnectReason, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété ExtendedDisconnectReason
topic_type:
- apiref
api_name:
- IMsRdpClient.ExtendedDisconnectReason
- IMsRdpClient.get_ExtendedDisconnectReason
- IMsRdpClient2.ExtendedDisconnectReason
- IMsRdpClient2.get_ExtendedDisconnectReason
- IMsRdpClient3.ExtendedDisconnectReason
- IMsRdpClient3.get_ExtendedDisconnectReason
- IMsRdpClient4.ExtendedDisconnectReason
- IMsRdpClient4.get_ExtendedDisconnectReason
- IMsRdpClient5.ExtendedDisconnectReason
- IMsRdpClient5.get_ExtendedDisconnectReason
- IMsRdpClient6.ExtendedDisconnectReason
- IMsRdpClient6.get_ExtendedDisconnectReason
- IMsRdpClient7.ExtendedDisconnectReason
- IMsRdpClient7.get_ExtendedDisconnectReason
- IMsRdpClient8.ExtendedDisconnectReason
- IMsRdpClient8.get_ExtendedDisconnectReason
- IMsRdpClient9.ExtendedDisconnectReason
- IMsRdpClient9.get_ExtendedDisconnectReason
- IMsRdpClient10.ExtendedDisconnectReason
- IMsRdpClient10.get_ExtendedDisconnectReason
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94c2612b231e24aaec855b6ebd1f9a0498b63c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509282"
---
# <a name="imsrdpclientextendeddisconnectreason-property"></a>IMsRdpClient :: ExtendedDisconnectReason, propriété

Contient des informations étendues sur la raison de la déconnexion du contrôle.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_ExtendedDisconnectReason(
  [out] ExtendedDisconnectReasonCode *pExtendedDisconnectReason
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur vers la valeur [**ExtendedDisconnectReasonCode**](extendeddisconnectreasoncode.md) indiquant la raison de la déconnexion du client.

## <a name="error-codes"></a>Codes d’erreur

Si la méthode est réussie, **S \_ OK** est retourné. Toute autre valeur **HRESULT** indique que l’appel a échoué.

## <a name="remarks"></a>Notes

En général, cette méthode est appelée dans le gestionnaire d’événements [**IMsTscAxEvents :: OnDisconnected**](imstscaxevents-ondisconnected.md) pour récupérer des informations supplémentaires sur l’événement de déconnexion.

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient est défini en tant que 92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





