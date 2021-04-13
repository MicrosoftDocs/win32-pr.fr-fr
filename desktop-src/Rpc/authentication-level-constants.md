---
title: Constantes Authentication-Level (rpcdce. h)
description: Les constantes de niveau d’authentification représentent les niveaux d’authentification passés à différentes fonctions d’exécution.
ms.assetid: b8bb2517-e1a0-4607-a672-259f8686fc3e
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_LEVEL_DEFAULT
- RPC_C_AUTHN_LEVEL_NONE
- RPC_C_AUTHN_LEVEL_CONNECT
- RPC_C_AUTHN_LEVEL_CALL
- RPC_C_AUTHN_LEVEL_PKT
- RPC_C_AUTHN_LEVEL_PKT_INTEGRITY
- RPC_C_AUTHN_LEVEL_PKT_PRIVACY
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114e5624b2cbc8af0b86a29daff2c1761f6fee39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509209"
---
# <a name="authentication-level-constants"></a>Constantes au niveau de l’authentification

Les constantes de niveau d’authentification représentent les niveaux d’authentification passés à différentes fonctions d’exécution. Ces niveaux sont répertoriés par ordre d’authentification accru. Chaque nouveau niveau ajoute à l’authentification fournie par le niveau précédent. Si la bibliothèque Runtime RPC ne prend pas en charge le niveau spécifié, elle est automatiquement mise à niveau vers le niveau immédiatement supérieur pris en charge.



| Constante                                                                                                                                                                                                                | Description                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <dt>**\_ \_ \_ valeur par défaut du niveau d’authentification RPC C \_**</dt> </dl>                    | Utilise le niveau d'authentification par défaut pour le service d'authentification spécifié.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <dt>**RPC \_ C \_ Authn \_ niveau \_ aucun**</dt> </dl>                             | N’effectue aucune authentification.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <dt>**\_ \_ \_ connexion au niveau AUTHn C RPC \_**</dt> </dl>                    | Effectue une authentification uniquement lorsque le client établit une relation avec un serveur.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <dt>**\_ \_ \_ appel au niveau d’authentification RPC C \_**</dt> </dl>                             | Authentifie uniquement au début de chaque appel de procédure distante lorsque le serveur reçoit la demande. Ne s’applique pas aux appels de procédure distante effectués à l’aide des séquences de protocole basées sur la connexion (celles qui commencent par le préfixe « ncacn »). Si la séquence de protocole dans un handle de liaison est une séquence de protocole basée sur la connexion et que vous spécifiez ce niveau, cette routine utilise à la place la \_ \_ constante PKT du niveau d’authentification RPC C \_ \_ .<br/> |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <dt>**protocole d’authentification de l' \_ authentification RPC C \_ \_ \_**</dt> </dl>                                | Authentifie uniquement que toutes les données reçues proviennent du client attendu. Ne valide pas les données elles-mêmes.<br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <dt>**\_ \_ \_ intégrité PKT du niveau d’authentification RPC \_ C \_**</dt> </dl> | Authentifie et vérifie qu’aucune des données transférées entre le client et le serveur n’a été modifiée.<br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <dt>**\_confidentialité du \_ niveau d’authentification RPC C \_ \_ \_**</dt> </dl>       | Comprend tous les niveaux précédents et garantit que les données en texte clair ne peuvent être consultées que par l’expéditeur et le destinataire. Dans le cas local, cela implique l’utilisation d’un canal sécurisé. Dans le cas distant, cela implique le chiffrement de la valeur d’argument de chaque appel de procédure distante.<br/>                                                                                                                                                                 |



## <a name="remarks"></a>Notes

Quelle que soit la valeur spécifiée par la constante, **Ncalrpc** utilise toujours le niveau de confidentialité de la \_ déclaration d’authentification RPC C \_ \_ \_ \_ .

## <a name="requirements"></a>Configuration requise



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

[**RpcMgmtInqDefaultProtectLevel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> <dt>

[**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[**RpcBindingInqAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

 





