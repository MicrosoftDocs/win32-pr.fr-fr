---
title: Constantes de délai d’attente de liaison (rpcdce. h)
description: La bibliothèque RPC utilise les constantes de délai d’expiration de liaison pour spécifier la durée relative à consacrer à l’établissement d’une liaison au serveur avant d’abandonner.
ms.assetid: bf5f3f08-ab29-4732-9ce3-d6d7ad699369
topic_type:
- apiref
api_name:
- RPC_C_BINDING_INFINITE_TIMEOUT
- RPC_C_BINDING_MIN_TIMEOUT
- RPC_C_BINDING_DEFAULT_TIMEOUT
- RPC_C_BINDING_MAX_TIMEOUT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d096fd320e1341f9affc35ae6ff1d355fcf12d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512564"
---
# <a name="binding-time-out-constants"></a>Constantes de délai d’attente de liaison

La bibliothèque RPC utilise les constantes de délai d’expiration de liaison pour spécifier la durée relative à consacrer à l’établissement d’une liaison au serveur avant d’abandonner. Le délai d’attente peut être activé à l’aide d’un appel à la fonction [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) . La liste suivante contient les valeurs de délai d’attente valides.



| Constante/valeur                                                                                                                                                                                                                                                                | Description                                                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_BINDING_INFINITE_TIMEOUT"></span><span id="rpc_c_binding_infinite_timeout"></span><dl> <dt>**RPC \_ \_Expiration de liaison C \_ infinie \_**</dt> <dt> 10</dt> </dl> | La tentative d’établissement de communications est définitive.<br/>                                                                                                                                                             |
| <span id="RPC_C_BINDING_MIN_TIMEOUT"></span><span id="rpc_c_binding_min_timeout"></span><dl> <dt>**RPC \_ \_ \_ \_ Délai d’expiration minimal de liaison C**</dt> <dt>0</dt> </dl>                   | Tente la durée minimale d’utilisation du protocole réseau. Cette valeur favorise le temps de réponse par rapport à l’exactitude pour déterminer si le serveur est en cours d’exécution.<br/>                                          |
| <span id="RPC_C_BINDING_DEFAULT_TIMEOUT"></span><span id="rpc_c_binding_default_timeout"></span><dl> <dt>**RPC \_ \_ \_ \_ Délai d’attente de liaison C par défaut**</dt> <dt>5</dt> </dl>       | Tente une durée moyenne pour le protocole réseau utilisé. Cette valeur donne l’exactitude de déterminer si un serveur est en cours d’exécution et donne un temps de réponse égal au poids. Il s’agit de la valeur par défaut.<br/> |
| <span id="RPC_C_BINDING_MAX_TIMEOUT"></span><span id="rpc_c_binding_max_timeout"></span><dl> <dt>**RPC \_ \_ \_ \_ Délai maximal de liaison C**</dt> <dt>9</dt> </dl>                   | Tente la durée la plus longue pour le protocole réseau utilisé. Cette valeur favorise l’exactitude pour déterminer si un serveur s’exécute sur le temps de réponse.<br/>                                            |



## <a name="remarks"></a>Notes

Les valeurs du tableau précédent ne sont pas en secondes. Ces valeurs représentent une durée relative sur une échelle de zéro à 10. Pour plus d’informations sur l’évitement des retards de communication, consultez la rubrique prévention des blocages côté client.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



 

 





