---
title: IMsRdpClient propriété SecuredSettings2
description: Récupère un pointeur vers l’interface IMsRdpClientSecuredSettings. Cette interface peut être utilisée pour définir des paramètres sécurisés pour le contrôle client.
ms.assetid: f570a3f6-70ae-45fd-ba20-75c9f4d2f5ca
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété SecuredSettings2
- Services Bureau à distance de la propriété SecuredSettings2, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété SecuredSettings2
- Services Bureau à distance de la propriété SecuredSettings2, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété SecuredSettings2
- Services Bureau à distance de la propriété SecuredSettings2, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété SecuredSettings2
- Services Bureau à distance de la propriété SecuredSettings2, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété SecuredSettings2
- Services Bureau à distance de la propriété SecuredSettings2, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété SecuredSettings2
- Services Bureau à distance de la propriété SecuredSettings2, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété SecuredSettings2
- Services Bureau à distance de la propriété SecuredSettings2, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété SecuredSettings2
- Services Bureau à distance de la propriété SecuredSettings2, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété SecuredSettings2
- Services Bureau à distance de la propriété SecuredSettings2, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété SecuredSettings2
- Services Bureau à distance de la propriété SecuredSettings2, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété SecuredSettings2
topic_type:
- apiref
api_name:
- IMsRdpClient.SecuredSettings2
- IMsRdpClient.get_SecuredSettings2
- IMsRdpClient2.SecuredSettings2
- IMsRdpClient2.get_SecuredSettings2
- IMsRdpClient3.SecuredSettings2
- IMsRdpClient3.get_SecuredSettings2
- IMsRdpClient4.SecuredSettings2
- IMsRdpClient4.get_SecuredSettings2
- IMsRdpClient5.SecuredSettings2
- IMsRdpClient5.get_SecuredSettings2
- IMsRdpClient6.SecuredSettings2
- IMsRdpClient6.get_SecuredSettings2
- IMsRdpClient7.SecuredSettings2
- IMsRdpClient7.get_SecuredSettings2
- IMsRdpClient8.SecuredSettings2
- IMsRdpClient8.get_SecuredSettings2
- IMsRdpClient9.SecuredSettings2
- IMsRdpClient9.get_SecuredSettings2
- IMsRdpClient10.SecuredSettings2
- IMsRdpClient10.get_SecuredSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39e26d9d7a7b2ac776166c251e5a2ab9923297f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508301"
---
# <a name="imsrdpclientsecuredsettings2-property"></a>IMsRdpClient :: SecuredSettings2, propriété

Récupère un pointeur vers l’interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) . Cette interface peut être utilisée pour définir des paramètres sécurisés pour le contrôle client.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_SecuredSettings2(
  [out] IMsRdpClientSecuredSettings **ppSecuredSettings
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur d’interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) .

## <a name="error-codes"></a>Codes d’erreur

Si la méthode est réussie, **S \_ OK** est retourné. Toute autre valeur **HRESULT** indique que l’appel a échoué.

## <a name="remarks"></a>Notes

Pour plus d’informations, consultez l’interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) et [fourniture de la sécurité du client RDP](providing-for-rdp-client-security.md).

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
</dt> </dl>

 

 





