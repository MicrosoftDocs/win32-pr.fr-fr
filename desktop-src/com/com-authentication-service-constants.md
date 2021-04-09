---
title: Constantes de service d’authentification (RpcDce. h)
description: Définit des services d’authentification en identifiant le package de sécurité qui fournit le service, tel que NTLMSSP, Kerberos ou Schannel.
ms.assetid: c16a8e52-a7f9-40d9-99ef-10b382b5cb3c
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
- RPC_C_AUTHN_KERNEL
- RPC_C_AUTHN_DIGEST
- RPC_C_AUTHN_NEGO_EXTENDER
- RPC_C_AUTHN_PKU2U
- RPC_C_AUTHN_MQ
- RPC_C_AUTHN_DEFAULT
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227d2accdf871c2e57a25661837d10089c983ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106318"
---
# <a name="authentication-service-constants"></a>Constantes de service d’authentification

Définit des services d’authentification en identifiant le package de sécurité qui fournit le service, tel que NTLMSSP, Kerberos ou Schannel.



| Constante/valeur                                                                                                                                                                                                                                               | Description                                                                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <dt>**RPC \_ C \_ Authn \_ None**</dt> <dt>0</dt> </dl>                              | Aucune authentification.<br/>                                                                                                                                                                                                                                                  |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <dt>**RPC \_ C \_ Authn \_ DCE \_ privé**</dt> <dt>1</dt> </dl>        | Authentification par clé privée DCE.<br/>                                                                                                                                                                                                                                     |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <dt>**RPC \_ C \_ Authn \_ DCE \_ public**</dt> <dt>2</dt> </dl>           | Authentification par clé publique DCE.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <dt>**RPC \_ C \_ Authn \_ Dec \_ public**</dt> <dt>4</dt> </dl>           | Authentification de la clé publique DEC. Réservé pour un usage futur.<br/>                                                                                                                                                                                                             |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <dt>**RPC \_ C \_ Authn \_ GSS \_ Negotiate**</dt> <dt>9</dt> </dl>  | Fournisseur de support de sécurité Snego.<br/>                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <dt>**RPC \_ C \_ Authn \_ winnt**</dt> <dt>10</dt> </dl>                          | NTLMSSP<br/>                                                                                                                                                                                                                                                             |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <dt>**RPC \_ C \_ Authn \_ GSS \_ Schannel**</dt> <dt>14</dt> </dl>    | Fournisseur de support de sécurité Schannel. Ce service d’authentification prend en charge les protocoles SSL 2,0, SSL 3,0, TLS et PCT.<br/>                                                                                                                                                            |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <dt>**RPC \_ C \_ Authn \_ GSS \_ Kerberos**</dt> <dt>16</dt> </dl>    | Fournisseur de support de sécurité Kerberos.<br/>                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <dt>**RPC \_ C \_ Authn \_ DPA**</dt> <dt>17</dt> </dl>                                | Fournisseur de support de sécurité DPA.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <dt>**RPC \_ C \_ Authn \_ MSN**</dt> <dt>18</dt> </dl>                                | Fournisseur de support de la sécurité MSN.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_KERNEL"></span><span id="rpc_c_authn_kernel"></span><dl> <dt>**RPC \_ C \_ Authn \_ noyau**</dt> <dt>20</dt> </dl>                       | Fournisseur de support de sécurité du noyau.<br/>                                                                                                                                                                                                                                   |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <dt>**RPC \_ C \_ Authn \_ Digest**</dt> <dt>21</dt> </dl>                       | Fournisseur de support de sécurité Digest.<br/>                                                                                                                                                                                                                                   |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <dt>**RPC \_ C \_ Authn \_ Nego \_ Extender**</dt> <dt>30</dt> </dl> | Fournisseur de support pour la sécurité de l’extendeur NEGO.<br/>                                                                                                                                                                                                                            |
| <span id="RPC_C_AUTHN_PKU2U"></span><span id="rpc_c_authn_pku2u"></span><dl> <dt>**RPC \_ C \_ Authn \_ PKU2U**</dt> <dt>31</dt> </dl>                          | Fournisseur de support de sécurité PKU2U.<br/>                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <dt>**RPC \_ C \_ Authn \_ MQ**</dt> <dt>100</dt> </dl>                                  | Fournisseur de support de sécurité MQ.<br/>                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <dt>**RPC \_ C \_ Authn \_ par défaut**</dt> <dt>0xFFFFFFFFL</dt> </dl>           | Service d’authentification par défaut du système. Lorsque cette valeur est spécifiée, COM utilise son algorithme de négociation permanente de sécurité normal pour choisir un service d’authentification. Pour plus d’informations, consultez [négociation de sécurité globale](security-blanket-negotiation.md). <br/> |



## <a name="remarks"></a>Notes

Ces constantes sont utilisées dans le [**seul \_ \_ service d’authentification**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) et dans les [**seules structures \_ d' \_ informations d’authentification**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) . La **seule structure du \_ \_ service d’authentification** est passée par le serveur à la fonction [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) et peut être récupérée par la fonction [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) . Un pointeur vers une structure d' **\_ \_ informations d’authentification unique** est passé par le client à **CoInitializeSecurity**. Pour plus d’informations sur les packages de sécurité identifiés par ces valeurs, tels que NTLMSSP et Kerberos, consultez [packages de sécurité et com](com-and-security-packages.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>RpcDce. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)
</dt> <dt>

[**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)
</dt> <dt>

[**\_informations d’authentification exclusives \_**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info)
</dt> <dt>

[**\_service d’authentification unique \_**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)
</dt> </dl>

 

