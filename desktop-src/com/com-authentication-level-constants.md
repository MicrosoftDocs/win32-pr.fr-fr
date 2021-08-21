---
title: Constantes de niveau d’authentification (rpcdce. h)
description: Ces valeurs spécifient un niveau d’authentification, qui indique la quantité d’authentification fournie pour aider à protéger l’intégrité des données. Chaque niveau comprend la protection fournie par les niveaux précédents.
ms.assetid: 06c409e4-3772-45cf-8c31-c64f99aca244
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
- rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcdcdf2ec566bafc962114d691c1962533b843d4c9299d01107eaaf132ea3050
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048677"
---
# <a name="authentication-level-constants"></a>Constantes de niveau d’authentification

Ces valeurs spécifient un niveau d’authentification, qui indique la quantité d’authentification fournie pour aider à protéger l’intégrité des données. Chaque niveau comprend la protection fournie par les niveaux précédents.



| Constante/valeur                                                                                                                                                                                                                                                                 | Description                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <dt>**RPC \_ \_ \_ \_ Valeur par défaut du niveau d’authentification C**</dt> <dt>0</dt> </dl>                    | Indique à DCOM de choisir le niveau d’authentification à l’aide de son algorithme de négociation permanente de sécurité normal. Pour plus d’informations, consultez [négociation de sécurité globale](security-blanket-negotiation.md). <br/> |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <dt>**RPC \_ C \_ Authn \_ niveau \_ aucun**</dt> <dt>1</dt> </dl>                             | N’effectue aucune authentification.<br/>                                                                                                                                                                         |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <dt>**RPC \_ \_ \_ \_ Connexion au niveau de l’authentification C**</dt> <dt>2</dt> </dl>                    | Authentifie les informations d’identification du client uniquement lorsque le client établit une relation avec le serveur. Les transports de datagrammes utilisent toujours l' \_ authentification PKT au niveau de l’authentification RPC \_ \_ . <br/>                        |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <dt>**RPC \_ \_ \_ \_ Appel de niveau Authn C**</dt> <dt>3</dt> </dl>                             | Authentifie uniquement au début de chaque appel de procédure distante lorsque le serveur reçoit la demande. Les transports de datagrammes utilisent à la place la procédure d' \_ authentification par authentification C RPC \_ \_ \_ .<br/>                                  |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <dt>**RPC \_ C \_ Authn \_ niveau \_ d’authentification PKT**</dt> <dt>4</dt> </dl>                                | Authentifie que toutes les données reçues proviennent du client attendu.<br/>                                                                                                                                   |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <dt>**RPC \_ \_ \_ \_ \_ Intégrité PKT de niveau d’authentification C**</dt> <dt>5</dt> </dl> | Authentifie et vérifie qu’aucune des données transférées entre le client et le serveur n’a été modifiée.<br/>                                                                                           |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <dt>**RPC \_ C Authentication \_ \_ PKT niveau de \_ \_ confidentialité**</dt> <dt>6</dt> </dl>       | Authentifie tous les niveaux précédents et chiffre la valeur d’argument de chaque appel de procédure distante.<br/>                                                                                                    |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



 

 





