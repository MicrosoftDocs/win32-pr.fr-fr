---
description: Supprime l’inscription des fournisseurs.
ms.assetid: e52c1ee0-140a-4277-bddd-d93338a512bc
title: CounterCleanup fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterCleanup
api_type:
- NA
api_location: ''
ms.openlocfilehash: eb768d3152aad5401c30b18a3f1ff13d1ef2397d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519902"
---
# <a name="countercleanup-function"></a>CounterCleanup fonction)

Supprime l’inscription du fournisseur.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI CounterCleanup(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Votre fournisseur appelle cette fonction. La fonction appelle la fonction [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) pour supprimer l’inscription du fournisseur.

L’outil [**CTRPP**](ctrpp.md) génère cette fonction inline lorsque vous spécifiez l’argument **-o** . Le nom de la fonction comprend une chaîne de *préfixe* si vous spécifiez l’argument **-prefix** (par exemple, **_prefix_CounterCleanup**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



 

 




