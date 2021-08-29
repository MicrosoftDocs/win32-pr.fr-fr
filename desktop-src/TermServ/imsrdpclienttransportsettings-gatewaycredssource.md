---
title: IMsRdpClientTransportSettings propriété GatewayCredsSource
description: Spécifie ou récupère la méthode d’authentification de la passerelle des services Bureau à Bureau à distance.
ms.assetid: 3b05edcb-f678-4d80-99fd-b76d27c80c68
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayCredsSource
- Services Bureau à distance de la propriété GatewayCredsSource, interface IMsRdpClientTransportSettings
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings, propriété GatewayCredsSource
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayCredsSource
- IMsRdpClientTransportSettings.get_GatewayCredsSource
- IMsRdpClientTransportSettings.put_GatewayCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0270d7123176161b2b90b423cde3d3945e15a179c3ffd5aa2335e079542c1098
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870869"
---
# <a name="imsrdpclienttransportsettingsgatewaycredssource-property"></a>IMsRdpClientTransportSettings :: GatewayCredsSource, propriété

Spécifie ou récupère la méthode d’authentification de la passerelle des services Bureau à Bureau à distance.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_GatewayCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a>Valeur de la propriété

Variable **ULong** qui spécifie la méthode d’authentification de la passerelle des services Bureau à distance. Ce paramètre peut prendre les valeurs suivantes.

<dt>

MODE d’identification du \_ proxy TSC \_ \_ \_ USERPASS (0)
</dt> <dd>

Utilisez un mot de passe (NTLM) comme méthode d’authentification pour la passerelle des services Bureau à distance.

</dd> <dt>

\_Carte à puce en mode d’identification TSC proxy \_ \_ \_ (1)
</dt> <dd>

Utilisez une carte à puce comme méthode d’authentification pour la passerelle des services Bureau à distance.

</dd> <dt>

MODE d’identification TSC du \_ proxy \_ \_ \_ Any (4)
</dt> <dd>

Utilisez n’importe quelle méthode d’authentification pour la passerelle des services Bureau à distance.

</dd> </dl>

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                   |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings est défini en tant que 720298C0-A099-46f5-9F82-96921BAE4701<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





