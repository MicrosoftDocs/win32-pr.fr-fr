---
title: Constantes d’autorisation (RpcDce. h)
description: Définit ce que le serveur autorise.
ms.assetid: a0bc9337-b7e4-41c5-ae36-4843fa7d98ce
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb89786a0c27c66177bc29861fdcf53a9341f73e498b5627e1cb826e83f61cc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048667"
---
# <a name="authorization-constants"></a>Constantes d’autorisation

Définit ce que le serveur autorise.



| Constante/valeur                                                                                                                                                                                                                                    | Description                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <dt>**RPC \_ C \_ authnt \_ aucun**</dt> <dt>0</dt> </dl>                   | Le serveur n’effectue aucune autorisation. Actuellement, RPC \_ c Authn \_ \_ WinNT, RPC \_ c \_ Authn \_ GSS \_ Schannel et RPC \_ c \_ Authn \_ GSS \_ Kerberos utilisent uniquement RPC \_ c \_ auth \_ aucun.<br/>                                                                                                                |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <dt>**RPC \_ \_ \_ Nom**</dt> d’autorisation C <dt>1</dt> </dl>                   | Le serveur effectue une autorisation basée sur le nom principal du client. <br/>                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <dt>**RPC \_ C \_ authz \_ DCE**</dt> <dt>2</dt> </dl>                      | Le serveur effectue une vérification d’autorisation à l’aide des informations de certificat PAC (Privileged attribute Certificate) du client, qui sont envoyées au serveur avec chaque appel de procédure distante effectué à l’aide du handle de liaison. En règle générale, l’accès est vérifié par rapport aux listes de contrôle d’accès (ACL) DCE. <br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <dt>**RPC \_ C \_ auth \_ par défaut**</dt> <dt>0xFFFFFFFF</dt> </dl> | DCOM peut choisir le niveau d’autorisation à l’aide de son algorithme de négociation permanente de sécurité normal. Pour plus d’informations, consultez [négociation de sécurité globale](security-blanket-negotiation.md).<br/>                                                                                           |



## <a name="remarks"></a>Remarques

Ces constantes sont utilisées par les méthodes de l’interface [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) . Ils sont utilisés dans la structure du [**\_ \_ service d’authentification unique**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) , qui est récupérée par la fonction [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) . Ils sont également utilisés dans la structure des [**\_ \_ informations d’authentification unique**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) , qui est, à son tour, membre de la structure de la [**\_ \_ liste d’authentification unique**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) . Cette structure, qui est une liste de services d’authentification, les services d’autorisation qu’elles exécutent et les informations d’authentification de chaque service, est passée à la fonction [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) et à la méthode [**IClientSecurity :: SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) .

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

 

