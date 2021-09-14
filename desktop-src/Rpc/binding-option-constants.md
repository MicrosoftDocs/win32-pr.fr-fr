---
title: Constantes d’option de liaison (rpcdce. h)
description: Les applications définissent les constantes d’option de liaison pour contrôler la façon dont la bibliothèque Runtime RPC traite les appels de procédure distante. Le tableau suivant répertorie chaque propriété de liaison et les valeurs de constante appropriées pour les propriétés de liaison.
ms.assetid: ff88e05d-b9f3-42ef-a44f-fee9261832c8
topic_type:
- apiref
api_name:
- RPC_C_OPT_BINDING_NONCAUSAL
- RPC_C_OPT_MAX_OPTIONS
- RPC_C_DONT_FAIL
- RPC_C_OPT_SESSION_ID
- RPC_C_OPT_COOKIE_AUTH
- RPC_C_OPT_RESOURCE_TYPE_UUID
- RPC_C_OPT_DONT_LINGER
- RPC_C_OPT_UNIQUE_BINDING
api_location:
- Rpcdce.h
- Rpcdcep.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52152b5ddcc17abe5c698697e30f1f1a512ee4f8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009163"
---
# <a name="binding-option-constants"></a>Constantes d’option de liaison

Les applications définissent les constantes d’option de liaison pour contrôler la façon dont la bibliothèque Runtime RPC traite les appels de procédure distante. Le tableau suivant répertorie chaque propriété de liaison et les valeurs de constante appropriées pour les propriétés de liaison.

> [!Note]  
> toutes les options de file d’attente de messages (MQ) dans le tableau suivant sont valides pour Windows 2000 uniquement. Windows XP et les versions ultérieures ne prennent pas en charge Message Queuing. Les développeurs sont déconseillés d’utiliser Message Queuing.

 



| Constante/valeur                                                                                                                                                                                                                                                        | Description                                                                                                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_OPT_BINDING_NONCAUSAL"></span><span id="rpc_c_opt_binding_noncausal"></span><dl> <dt>**RPC \_ \_Liaison opt \_ \_ C**</dt> pour une liaison inversée <dt>9</dt> </dl>     | Par défaut. Si la **valeur est false**, l’ordre de causalité. Les appels RPC sont exécutés dans un ordre strict d’envoi. Consultez la section Notes.<br/> Si la **valeur est true**, ordre des appels à la causalité. Les appels RPC sont exécutés indépendamment. Consultez la section Notes.<br/>                                                                        |
| <span id="RPC_C_OPT_MAX_OPTIONS"></span><span id="rpc_c_opt_max_options"></span><dl> <dt>**RPC \_ \_ \_ \_ Options Max opt Max**</dt> . <dt>17</dt> </dl>                      | Non nécessaire pour les programmes d’application. Utilisé en interne par Microsoft.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_DONT_FAIL"></span><span id="rpc_c_dont_fail"></span><dl> <dt>**RPC \_ C \_ \_ ne pas réussir**</dt> <dt>4</dt> </dl>                                          | Non nécessaire pour les programmes d’application. Utilisé en interne par Microsoft.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_OPT_SESSION_ID"></span><span id="rpc_c_opt_session_id"></span><dl> <dt>**RPC \_ C \_ OPT \_ session \_ ID**</dt> <dt>6</dt> </dl>                          | Si la **valeur est true**, un ID de session est généré pour chaque connexion.<br/>                                                                                                                                                                                                                                |
| <span id="RPC_C_OPT_COOKIE_AUTH"></span><span id="rpc_c_opt_cookie_auth"></span><dl> <dt>**RPC \_ C \_ OPT \_ cookie \_ auth**</dt> <dt>7</dt> </dl>                       | Si la **valeur est true**, l’authentification basée sur les cookies côté client est utilisée pour les connexions. Un pointeur vers la structure du [**\_ \_ \_ \_ \_ descripteur d’authentification de cookie RPC C opt**](/windows/desktop/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor) est passé en tant que paramètre *OptionValue* dans [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption).<br/> |
| <span id="RPC_C_OPT_RESOURCE_TYPE_UUID"></span><span id="rpc_c_opt_resource_type_uuid"></span><dl> <dt>**RPC \_ \_UUID de \_ \_ type de \_ ressource OPT**</dt> <dt>8</dt> </dl> | Non nécessaire pour les programmes d’application. Utilisé en interne par Microsoft.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_OPT_DONT_LINGER"></span><span id="rpc_c_opt_dont_linger"></span><dl> <dt>**RPC \_ C \_ OPT \_ \_**</dt> ne pas attendre <dt>13</dt> </dl>                      | Si la **valeur est true**, forcer l’arrêt de l’Association après le dernier handle de liaison/handle de contexte sur celui-ci est libéré.<br/>                                                                                                                                                                                |
| <span id="RPC_C_OPT_UNIQUE_BINDING"></span><span id="rpc_c_opt_unique_binding"></span><dl> <dt>**RPC \_ C \_ OPT \_ unique \_ liaison unique**</dt> <dt>11</dt> </dl>             | Si la valeur est **true**, RPC ne réutilise pas les connexions existantes. Un handle de liaison unique est ouvert pour chaque connexion et l’État est conservé pour chaque handle de liaison unique.<br/>                                                                                                               |



## <a name="remarks"></a>Notes

Par défaut, la bibliothèque Runtime RPC exécute les appels sur un handle de liaison donné à partir de chaque thread d’une application dans un ordre strict d’envoi. Cela ne garantit pas que les appels de différents threads sur le même handle de liaison sont sérialisés. Les applications multithread doivent sérialiser leurs appels RPC. Si ce comportement est trop restrictif, vous pouvez activer le classement non-causalité. Dans ce cas, la bibliothèque Runtime RPC exécute les appels indépendamment. Il n’impose aucun ordre d’envoi.

Un exemple d’application susceptible de trouver un ordre non-causalité utile est un programme multithread dont les threads effectuent des appels sur le même handle de liaison. De même, un programme qui utilise plusieurs appels asynchrones sur un handle de liaison trouvera une option pratique qui est pratique. Un autre exemple peut être un programme de proxy Internet qui utilise un thread unique pour gérer les demandes de plusieurs clients. Dans chacun de ces cas, il serait extrêmement restrictif d’essayer de sérialiser les appels de procédure distante.

L’option de non- **\_ acceptation RPC C \_ OPT \_ \_** ne peut être définie que sur des handles de liaison qui utilisent les séquences de protocole **Ncalrpc** ou **ncacn \_ \** _. Elle ne peut pas être utilisée sur les séquences de protocole _*ncadg \_ \**_ . La fonction [_ *RpcBindingSetOption* *](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) avec cette option doit être appelée sur un handle de liaison sur lequel au moins un appel RPC a été effectué. Si aucun appel RPC n’a été effectué sur le handle de liaison, le **\_ \_ \_ type \_ de \_ liaison RPC S incorrect** est retourné à partir de l’appel de fonction **RpcBindingSetOption** . L’option prend effet pour l’ensemble de l’Association, quel que soit le nombre de descripteurs de liaisons attachés à l’Association. Étant donné qu’elle est vérifiée avant la destruction de l’Association, elle peut être définie à tout moment avant la fermeture du handle de liaison.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                 |
| En-tête<br/>                   | <dl> <dt>Rpcdce. h ; </dt> <dt>Rpcdcep. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[**RpcBindingInqOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[Gestion des groupes de connexions réseau (associations)](managing-network-connection-sets-associations-.md)
</dt> </dl>

 

 





