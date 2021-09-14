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
ms.openlocfilehash: 085d5c59b17b10949ad39d07354906f40e123988
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021046"
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

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est **true** et la fonction retourne les informations demandées.

Si la fonction échoue, la valeur de retour est **false**.

## <a name="remarks"></a>Notes

Le membre **version** de la structure [**EXPERTENUMINFO**](expertenuminfo.md) doit être égal à zéro.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




