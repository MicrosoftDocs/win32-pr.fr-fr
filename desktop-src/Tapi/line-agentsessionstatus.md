---
description: Le \_ message de ligne AGENTSESSIONSTATUS est envoyé lorsque l’état d’une session de l’agent ACD change sur un gestionnaire d’agent pour lequel l’application a actuellement une ligne ouverte. Ce message est généré à l’aide de la fonction lineProxyMessage.
ms.assetid: bb9d2292-8c41-4557-989e-6c5eb785313f
title: Message LINE_AGENTSESSIONSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25209abda7cfec3864c45bfd58a35a9fad21a1aa5e5645669a7fdad6ec907d5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003217"
---
# <a name="line_agentsessionstatus-message"></a>\_Message AGENTSESSIONSTATUS de ligne

Le message de **ligne \_ AGENTSESSIONSTATUS** est envoyé lorsque l’état d’une session de l’agent ACD change sur un gestionnaire d’agent pour lequel l’application a actuellement une ligne ouverte. Ce message est généré à l’aide de la fonction [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .


```C++
        
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwDevice* 
</dt> <dd>

Handle de l’application sur le périphérique de ligne sur lequel l’état de session de l’agent a été modifié.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instance de rappel fournie lors de l’ouverture de la ligne.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Handle de la session de l’agent dont l’État a changé.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Spécifie l’état de session de l’agent qui a changé. Il peut s’agir d’une ou plusieurs **lignes \_ AGENTSESSIONSTATUS**.

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

[**lineGetAgentSessionInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo)
</dt> <dt>

[**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




