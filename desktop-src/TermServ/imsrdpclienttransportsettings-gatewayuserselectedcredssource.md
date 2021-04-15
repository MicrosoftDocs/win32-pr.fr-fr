---
title: IMsRdpClientTransportSettings propriété GatewayUserSelectedCredsSource
description: Définit ou récupère la source des informations d’identification spécifiées par l’utilisateur Bureau à distance passerelle des services Bureau à distance.
ms.assetid: 0c12ddf6-52c2-40a2-af2b-effd4e8bbdb6
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayUserSelectedCredsSource
- Services Bureau à distance de la propriété GatewayUserSelectedCredsSource, interface IMsRdpClientTransportSettings
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings, propriété GatewayUserSelectedCredsSource
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.get_GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.put_GatewayUserSelectedCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1556088e62221df7ff91b4b0069bb1ec938ebf23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508382"
---
# <a name="imsrdpclienttransportsettingsgatewayuserselectedcredssource-property"></a>IMsRdpClientTransportSettings :: GatewayUserSelectedCredsSource, propriété

Définit ou récupère la source des informations d’identification spécifiées par l’utilisateur Bureau à distance passerelle des services Bureau à distance.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_GatewayUserSelectedCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayUserSelectedCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a>Valeur de la propriété

Variable **ULong** qui spécifie la méthode d’authentification de la passerelle des services Bureau à distance. Ce paramètre peut prendre les valeurs suivantes.

<dt>

<span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>

<span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>**TSC \_ MODE d’identification du PROXY \_ \_ \_ USERPASS** (0 (0x0))


</dt> <dd>

Utilisez un mot de passe (NTLM) comme méthode d’authentification pour la passerelle des services Bureau à distance.

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>

<span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>**TSC \_ \_ \_ \_ Carte à puce mode** d’identification du proxy (1 (0x1))


</dt> <dd>

Utilisez une carte à puce comme méthode d’authentification pour la passerelle des services Bureau à distance.

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>

<span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>**TSC \_ \_ \_ Mode \_ d’identification du proxy any** (4 (0x4))


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

 

 





