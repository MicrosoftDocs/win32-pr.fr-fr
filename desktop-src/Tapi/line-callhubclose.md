---
description: Le \_ message CALLHUBCLOSE de ligne TAPI est envoyé lorsqu’un hub d’appel a été fermé.
ms.assetid: 738dcb20-99b5-44fe-8ad9-b14b8d977f53
title: Message LINE_CALLHUBCLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b538d6f154f3dacb2d779b6233722df16cc635d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217836"
---
# <a name="line_callhubclose-message"></a>\_Message CALLHUBCLOSE de ligne

Le message **\_ CALLHUBCLOSE de ligne** TAPI est envoyé lorsqu’un hub d’appel a été fermé.


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

Réservé. Définit la valeur 0.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Réservé. Définit la valeur 0.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Réservé. Définit la valeur 0.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Ce message provient de l’interface TAPI plutôt que d’un fournisseur de services, ce qui signifie qu’il n’y a aucun message TSPI correspondant.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,2<br/>                                                      |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




