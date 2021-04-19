---
description: Le message CALLINFO de ligne TAPI \_ est envoyé lorsque les informations sur l’appel de l’appel spécifié ont été modifiées. L’application peut appeler lineGetCallInfo pour déterminer les informations d’appel actuelles.
ms.assetid: eb882409-6842-434e-9f93-61cf0c11d1d0
title: Message LINE_CALLINFO (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6005ab5383816ead440f5a1a7d580bfaccb5c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541114"
---
# <a name="line_callinfo-message"></a>\_Message CALLINFO de ligne

Le message **\_ CALLINFO de ligne** TAPI est envoyé lorsque les informations sur l’appel de l’appel spécifié ont été modifiées. L’application peut appeler [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) pour déterminer les informations d’appel actuelles.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle de l’appel.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instance de rappel fournie lors de l’ouverture de la ligne de l’appel.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Élément d’informations d’appel qui a changé. Il peut s’agir d’une ou plusieurs des [**\_ constantes LINECALLINFOSTATE**](linecallinfostate--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Inutilisé.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Inutilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Un **message \_ CALLINFO de ligne** avec une indication *NumOwnersIncr*, *NumOwnersDecr* et/ou *NumMonitorsChanged* est envoyé aux applications qui ont déjà un handle pour l’appel. Cela peut être le résultat d’une autre application modifiant la propriété ou la surveillance d’un appel avec [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen), [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose), [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown), [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege), [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)et [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls).

Ces **messages \_ CALLINFO de ligne** ne sont pas envoyés lorsqu’une notification d’un nouvel appel est fournie dans un message de [**ligne \_ CALLSTATE**](line-callstate.md) , car les informations d’appel reflètent déjà le nombre correct de propriétaires et de moniteurs au moment où la ligne \_ CALLSTATE messages sont envoyées. **Ligne \_** Les messages CALLINFO sont également supprimés dans le cas où un appel est offert par l’interface TAPI à des analyses via le \_ mécanisme LINECALLSTATE inconnu.

> [!Note]  
> L’application qui provoque une modification du nombre de propriétaires ou d’analyses (par exemple, en appelant [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) ou [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)) ne reçoit pas lui-même un message indiquant que la modification a été effectuée.

 

Aucun **message \_ CALLINFO de ligne** n’est envoyé pour un appel une fois que l’appel est passé à l’état *inactif* . Plus précisément, les modifications du nombre de propriétaires et de moniteurs ne sont pas signalées, car les applications libèrent leurs Handles pour l’appel inactif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)
</dt> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)
</dt> <dt>

[**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




