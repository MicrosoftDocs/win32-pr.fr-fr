---
description: Le \_ message APPNEWCALLHUB de ligne TAPI est envoyé pour informer une application quand un nouveau hub d’appel a été créé.
ms.assetid: cf693d95-9abb-4999-81b6-7d2aa06d0f58
title: Message LINE_APPNEWCALLHUB (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bf413f16270ba54fd7447cc0c41c040759edd699c995eac79314b9961486ce5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905902"
---
# <a name="line_appnewcallhub-message"></a>\_Message APPNEWCALLHUB de ligne

Le message **\_ APPNEWCALLHUB de ligne** TAPI est envoyé pour informer une application quand un nouveau hub d’appel a été créé.


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

Le niveau de suivi sur le nouveau Hub, tel que défini par l’une des [**\_ constantes LINECALLHUBTRACKING**](linecallhubtracking--constants.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Ce message provient de l’interface TAPI plutôt que d’un fournisseur de services, ce qui signifie qu’il n’y a aucun message TSPI correspondant.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,2<br/>                                                      |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




