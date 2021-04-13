---
title: IMsRdpClientTransportSettings3 propriété GatewayEncryptedAuthCookieSize
description: Taille, en caractères, de la propriété GatewayEncryptedAuthCookie.
ms.assetid: 52e24bef-5afa-4954-b639-08ea8701404a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayEncryptedAuthCookieSize
- Services Bureau à distance de la propriété GatewayEncryptedAuthCookieSize, interface IMsRdpClientTransportSettings3
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings3, propriété GatewayEncryptedAuthCookieSize
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayEncryptedAuthCookieSize
- IMsRdpClientTransportSettings3.get_GatewayEncryptedAuthCookieSize
- IMsRdpClientTransportSettings3.put_GatewayEncryptedAuthCookieSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 238245cdb9c0164b69434cf61f790b8f81fa3da2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465790"
---
# <a name="imsrdpclienttransportsettings3gatewayencryptedauthcookiesize-property"></a>IMsRdpClientTransportSettings3 :: GatewayEncryptedAuthCookieSize, propriété

Taille, en caractères, de la propriété [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) .

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_GatewayEncryptedAuthCookieSize(
  [in]          ULONG ulEncryptedAuthCookieSize
);

HRESULT get_GatewayEncryptedAuthCookieSize(
  [out, retval] ULONG *ulEncryptedAuthCookieSize
);
```



## <a name="property-value"></a>Valeur de la propriété

Valeur **ULong** qui contient la nouvelle valeur de taille.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





