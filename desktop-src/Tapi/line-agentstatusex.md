---
description: Le \_ message de ligne AGENTSTATUSEX est envoyé lorsque l’état d’un agent ACD change sur un gestionnaire d’agent pour lequel l’application a actuellement une ligne ouverte. Ce message est généré à l’aide de la fonction lineProxyMessage.
ms.assetid: a0709367-9105-43af-9772-0161d94c098a
title: Message LINE_AGENTSTATUSEX (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abc622d1df7b9d86009822f9920cf9f510c68b71a28952a4146e98bdbe69e9da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119405220"
---
# <a name="line_agentstatusex-message"></a>\_Message AGENTSTATUSEX de ligne

Le message de **ligne \_ AGENTSTATUSEX** est envoyé lorsque l’état d’un agent ACD change sur un gestionnaire d’agent pour lequel l’application a actuellement une ligne ouverte. Ce message est généré à l’aide de la fonction [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .


```C++
        
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwDevice* 
</dt> <dd>

Handle de l’application sur le périphérique de ligne. Cela est relatif au gestionnaire de l’agent.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instance de rappel fournie lors de l’ouverture de la ligne.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Handle de l’agent dont l’État a changé.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Spécifie l’état de la file d’attente qui a changé. Il peut s’agir d’une ou plusieurs des [**\_ constantes LINEQUEUESTATUS**](linequeuestatus--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Si *dwParam2* comprend le \_ bit d’État LINEAGENTSTATUSEX, *dwParam3* indique la nouvelle valeur de l’état de l’agent, qui est l’une des [**\_ constantes LINEAGENTSTATEEX**](lineagentstateex--constants.md).

Sinon, *dwParam3* a la valeur zéro.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,2<br/>                                                      |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**lineGetAgentInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo)
</dt> <dt>

[**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




