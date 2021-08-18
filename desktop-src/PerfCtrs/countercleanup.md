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
ms.openlocfilehash: fe06923849a12609b6662505df94c927c3d9dfd4aeb8bc6a42bd6a225e042ef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011367"
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

## <a name="remarks"></a>Remarques

Votre fournisseur appelle cette fonction. La fonction appelle la fonction [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) pour supprimer l’inscription du fournisseur.

L’outil [**CTRPP**](ctrpp.md) génère cette fonction inline lorsque vous spécifiez l’argument **-o** . Le nom de la fonction comprend une chaîne de *préfixe* si vous spécifiez l’argument **-prefix** (par exemple, **_prefix_CounterCleanup**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



 

 




