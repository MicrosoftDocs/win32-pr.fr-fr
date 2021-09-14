---
title: Constantes Authorization-Service (rpcdce. h)
description: Les constantes de service d’autorisation représentent les services d’autorisation passés à différentes fonctions d’exécution.
ms.assetid: b773bb51-7af0-4eb3-9438-fe3ef9a350db
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0394163e97a822126e71eeda3cf8382f1dcc20
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416619"
---
# <a name="authorization-service-constants"></a>Constantes Authorization-Service

Les constantes de service d’autorisation représentent les services d’autorisation passés à différentes fonctions d’exécution.

Les constantes suivantes sont des valeurs valides pour le paramètre *AuthzSvc* . La plupart des applications recherchent une autorisation RPC \_ C \_ \_ insuffisante.



| Constante/valeur                                                                                                                                                                                                                                    | Description                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <dt>**RPC \_ C \_ authnt \_ aucun**</dt> <dt>0</dt> </dl>                   | Le serveur n’effectue aucune autorisation.<br/>                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <dt>**RPC \_ \_ \_ Nom**</dt> d’autorisation C <dt>1</dt> </dl>                   | Le serveur effectue une autorisation basée sur le nom principal du client.<br/>                                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <dt>**RPC \_ C \_ authz \_ DCE**</dt> <dt>2</dt> </dl>                      | Le serveur effectue une vérification d’autorisation à l’aide des informations de certificat PAC (Privileged attribute Certificate) du client, qui sont envoyées au serveur avec chaque appel de procédure distante effectué à l’aide du handle de liaison. En règle générale, l’accès est vérifié par rapport aux listes de contrôle d’accès ([ACL](/windows/desktop/api/winnt/ns-winnt-acl)) DCE.<br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <dt>**RPC \_ C \_ auth \_ par défaut**</dt> <dt>0xFFFFFFFF</dt> </dl> | Le serveur utilise le service d’autorisation par défaut pour le fournisseur de services partagés actuel.<br/>                                                                                                                                                                                                                                |



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
</dt> <dt>

[**RpcMgmtInqDefaultProtectLevel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> </dl>

 

