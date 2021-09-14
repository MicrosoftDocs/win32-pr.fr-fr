---
title: Constantes Authentication-Service (rpcdce. h)
description: Les constantes de service d’authentification représentent les services d’authentification passés à différentes fonctions d’exécution.
ms.assetid: ac95276f-230d-4993-92fe-1739d022c8b3
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_NONE
- RPC_C_AUTHN_DCE_PRIVATE
- RPC_C_AUTHN_DCE_PUBLIC
- RPC_C_AUTHN_DEC_PUBLIC
- RPC_C_AUTHN_GSS_NEGOTIATE
- RPC_C_AUTHN_WINNT
- RPC_C_AUTHN_GSS_SCHANNEL
- RPC_C_AUTHN_GSS_KERBEROS
- RPC_C_AUTHN_DPA
- RPC_C_AUTHN_MSN
- RPC_C_AUTHN_DIGEST
- RPC_C_AUTHN_NEGO_EXTENDER
- RPC_C_AUTHN_MQ
- RPC_C_AUTHN_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4ace510c1c26030542090eb1b00e76db803df6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123494"
---
# <a name="authentication-service-constants"></a>Constantes Authentication-Service

Les constantes de service d’authentification représentent les services d’authentification passés à différentes fonctions d’exécution.

Les constantes suivantes sont des valeurs valides pour le paramètre *AuthnSvc* .



| Constante/valeur                                                                                                                                                                                                                                               | Description                                                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <dt>**RPC \_ C \_ Authn \_ None**</dt> <dt>0</dt> </dl>                              | Aucune authentification.<br/>                                                                                                                                                        |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <dt>**RPC \_ C \_ Authn \_ DCE \_ privé**</dt> <dt>1</dt> </dl>        | Utilisez l’authentification par clé privée DCE (Distributed Computing Environment).<br/>                                                                                                   |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <dt>**RPC \_ C \_ Authn \_ DCE \_ public**</dt> <dt>2</dt> </dl>           | Authentification par clé publique DCE (réservée à une utilisation ultérieure).<br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <dt>**RPC \_ C \_ Authn \_ Dec \_ public**</dt> <dt>4</dt> </dl>           | Authentification par clé publique DEC (réservée à une utilisation ultérieure).<br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <dt>**RPC \_ C \_ Authn \_ GSS \_ Negotiate**</dt> <dt>9</dt> </dl>  | Utilisez le [SSP Microsoft Negotiate](/windows/desktop/SecAuthN/microsoft-negotiate). Ce SSP négocie entre l’utilisation des fournisseurs SSP (Security Support Provider) NTLM et Kerberos.<br/>  |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <dt>**RPC \_ C \_ Authn \_ winnt**</dt> <dt>10</dt> </dl>                          | Utilisez le [SSP Microsoft NT LAN Manager (NTLM)](/windows/desktop/SecAuthN/microsoft-ntlm).<br/>                                                                                                   |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <dt>**RPC \_ C \_ Authn \_ GSS \_ Schannel**</dt> <dt>14</dt> </dl>    | Utilisez le [SSP Schannel](/windows/desktop/SecAuthN/secure-channel). Ce fournisseur de services partagés prend en charge le protocole SSL (Secure Socket Layer), PCT (Private Communication Technology) et TLS (Transport Level Security).<br/> |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <dt>**RPC \_ C \_ Authn \_ GSS \_ Kerberos**</dt> <dt>16</dt> </dl>    | Utilisez le [SSP Microsoft Kerberos](/windows/desktop/SecAuthN/microsoft-kerberos).<br/>                                                                                                            |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <dt>**RPC \_ C \_ Authn \_ DPA**</dt> <dt>17</dt> </dl>                                | Utilisez l’authentification par mot de passe distribué (DPA).<br/>                                                                                                                            |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <dt>**RPC \_ C \_ Authn \_ MSN**</dt> <dt>18</dt> </dl>                                | Protocole SSP du protocole d’authentification utilisé pour Microsoft Network (MSN).<br/>                                                                                                         |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <dt>**RPC \_ C \_ Authn \_ Digest**</dt> <dt>21</dt> </dl>                       | Windows XP ou version ultérieure : utiliser le [SSP Microsoft Digest](/windows/desktop/SecAuthN/microsoft-digest-ssp)<br/>                                                                                        |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <dt>**RPC \_ C \_ Authn \_ Nego \_ Extender**</dt> <dt>30</dt> </dl> | Windows 7 ou version ultérieure : réservé. À ne pas utiliser<br/>                                                                                                                                  |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <dt>**RPC \_ C \_ Authn \_ MQ**</dt> <dt>100</dt> </dl>                                  | Ce fournisseur de services partagés fournit un wrapper compatible SSPI pour le protocole de niveau transport MSMQ (Microsoft Message Queue).<br/>                                                             |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <dt>**RPC \_ C \_ Authn \_ par défaut**</dt> <dt>0xFFFFFFFF</dt> </dl>            | Utilisez le service d’authentification par défaut.<br/>                                                                                                                                   |



## <a name="remarks"></a>Notes

Spécifiez RPC \_ C \_ Authn \_ None pour désactiver l’authentification pour les appels de procédure distante effectués sur un handle de liaison. Lorsque vous spécifiez \_ \_ \_ la valeur par défaut RPC c Authn, la bibliothèque Runtime RPC utilise \_ le \_ \_ service d’authentification Winnt RPC c Authn pour les appels de procédure distante effectués à l’aide du handle de liaison.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RpcBindingInqAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[**RpcBindingInqAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

