---
description: Le \_ message AGENTSPECIFIC de ligne TAPI est envoyé lorsque l’état d’un agent ACD change sur une ligne ouverte par l’application. L’application peut appeler lineGetAgentStatus pour déterminer l’état actuel de l’agent.
ms.assetid: 67e1796c-02e5-4f81-8086-7c2ff3112ae0
title: Message LINE_AGENTSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ca03138ce00f11520e2e0f1df8e810e21d1186
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544107"
---
# <a name="line_agentspecific-message"></a>\_Message AGENTSPECIFIC de ligne

Le message **\_ AGENTSPECIFIC de ligne** TAPI est envoyé lorsque l’état d’un agent ACD change sur une ligne ouverte par l’application. L’application peut appeler [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) pour déterminer l’état actuel de l’agent.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle de l’application sur le périphérique de ligne.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instance de rappel fournie lors de l’ouverture de la ligne de l’appel.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Index dans le tableau d’identificateurs d’extension de gestionnaire dans la structure [**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) de l’extension de gestionnaire à laquelle le message est associé.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Spécifique à l’extension du gestionnaire. En règle générale, cette valeur est utilisée pour forcer l’application à appeler une fonction [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) pour extraire plus de détails sur le message.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Spécifique à l’extension du gestionnaire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Le message de **ligne \_ AGENTSPECIFIC** n’est pas envoyé aux applications qui prennent en charge des versions antérieures de TAPI.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)
</dt> <dt>

[**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)
</dt> <dt>

[**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




