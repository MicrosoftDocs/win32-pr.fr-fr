---
description: L’expert doit implémenter la fonction d’expert d’inscription. Moniteur réseau appelle la fonction d’expert Register pour obtenir des informations sur l’expert.
ms.assetid: 58cfe525-99b1-40ce-b8d8-fa1c62a20c40
title: Inscrire la fonction de rappel d’expert (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 1203682e82b01b7665c9661c3f58c14bbf2cd479cac62c72a64505b0e25feaa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889569"
---
# <a name="register-expert-callback-function"></a>Enregistrer la fonction de rappel d’expert

L’expert doit implémenter la fonction d’expert d' **inscription** . Moniteur réseau appelle la fonction d’expert **Register** pour obtenir des informations sur l’expert.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI Register(
  _Inout_ PEXPERTENUMINFO pExpertInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pExpertInfo* \[ in, out\]
</dt> <dd>

Pointeur vers une structure [**EXPERTENUMINFO**](expertenuminfo.md) qui Moniteur réseau alloue. L’expert remplit la structure avec toutes les informations demandées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est **true** et la fonction retourne les informations demandées.

Si la fonction échoue, la valeur de retour est **false**.

## <a name="remarks"></a>Remarques

Le membre **version** de la structure [**EXPERTENUMINFO**](expertenuminfo.md) doit être égal à zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




