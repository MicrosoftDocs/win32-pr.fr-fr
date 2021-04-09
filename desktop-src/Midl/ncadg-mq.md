---
title: attribut ncadg_mq
description: Le \_ mot clé ncadg MQ identifie Microsoft Message Queuing services (MSMQ) comme protocole de transport pour le point de terminaison. Ce protocole est obsolète et ne doit pas être utilisé dans les nouvelles applications.
ms.assetid: 7472fc47-c1f0-4578-8aef-b655505e0563
keywords:
- ncadg_mq MIDL de l’attribut
topic_type:
- apiref
api_name:
- ncadg_mq
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0acc433b55ba9f3c6d8919bef9b8db470bc0f5a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940907"
---
# <a name="ncadg_mq-attribute"></a>\_attribut MQ ncadg

Le mot clé **ncadg \_ MQ** identifie Microsoft Message QUEUING services (MSMQ) comme protocole de transport pour le point de terminaison. Ce protocole est obsolète et ne doit pas être utilisé dans les nouvelles applications.

``` syntax
endpoint("ncadg_mq:server-name")
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom du serveur* 
</dt> <dd>

Spécifie le nom du serveur ou de l’ordinateur hôte. Le nom est une chaîne de caractères et peut être un nom de domaine complet.

</dd> </dl>

## <a name="remarks"></a>Notes

Pour pouvoir utiliser le protocole de transport **ncadg \_ MQ** , les composants MSMQ doivent être entièrement installés et les systèmes client et serveur doivent être accessibles via les protocoles mq.

Le protocole **ncadg \_ MQ** ne prend pas en charge les points de terminaison ou les appels de [**diffusion**](broadcast.md) dynamiques. Comme avec les autres protocoles de datagramme, **ncadg \_ MQ** ne prend pas en charge les rappels ; les fonctions qui utilisent l’attribut de [**rappel**](callback.md) échouent.

> [!Note]  
> Cette famille de protocoles n’est pas prise en charge dans WindowsÂ XP.

 

## <a name="examples"></a>Exemples

La syntaxe du protocole de file d’attente de messages est définie indépendamment de la spécification IDL. Le compilateur MIDL effectue une vérification de la syntaxe, mais ne garantit pas que la spécification du point de terminaison est correcte. Certaines erreurs peuvent être signalées au moment de l’exécution plutôt que pendant la compilation.

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_mq:rainier") 
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**diffusion**](broadcast.md)
</dt> <dt>

[**rappel**](callback.md)
</dt> <dt>

[**poste**](endpoint.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Message**](message.md)
</dt> <dt>

[Message Queuing RPC](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[Liaison de chaîne](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 