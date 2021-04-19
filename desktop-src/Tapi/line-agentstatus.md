---
description: Le \_ message AGENTSTATUS de ligne TAPI est envoyé lorsque l’état d’un agent ACD change sur une ligne ouverte par l’application. L’application peut appeler lineGetAgentStatus pour déterminer l’état actuel de l’agent.
ms.assetid: 48f5d9bc-f20d-4364-8ec1-0b4bdc9cfcb4
title: Message LINE_AGENTSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b98242745e2f025f95cfe06fbe22c8956a02b0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521664"
---
# <a name="line_agentstatus-message"></a>\_Message AGENTSTATUS de ligne

Le message **\_ AGENTSTATUS de ligne** TAPI est envoyé lorsque l’état d’un agent ACD change sur une ligne ouverte par l’application. L’application peut appeler [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) pour déterminer l’état actuel de l’agent.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle de l’application sur le périphérique de ligne sur lequel l’état de l’agent a changé.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instance de rappel fournie lors de l’ouverture de la ligne de l’appel.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificateur de l’adresse sur la ligne sur laquelle l’état de l’agent a été modifié. Un identificateur d’adresse est associé de manière permanente à une adresse ; l’identificateur reste constant entre les mises à niveau du système d’exploitation.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Spécifie l’état de l’agent qui a changé ; peut être une combinaison de [**\_ constantes LINEAGENTSTATUS**](lineagentstatus--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Si *dwParam2* comprend le \_ bit d’État LINEAGENTSTATUS, *dwParam3* indique la nouvelle valeur du membre **dwState** dans [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus). Dans le cas contraire, ce paramètre a la valeur zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Le message de **ligne \_ AGENTSTATUS** n’est pas envoyé aux applications qui prennent en charge des versions antérieures de TAPI.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)
</dt> <dt>

[**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




