---
title: Méthode IMemoryAllocator Free
description: La méthode Free libère la mémoire allouée par la méthode Allocate.
ms.assetid: 41f81cba-4431-4ff7-ac84-8ff5bea71b65
keywords:
- Stockage structurée de la méthode libre
- Stockage structurée de la méthode libre, interface IMemoryAllocator
- Stockage structurée de l’interface IMemoryAllocator, méthode libre
topic_type:
- apiref
api_name:
- IMemoryAllocator.Free
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f78690a37b5500f5e540cf4c2ef516b7c3ea89c219ba475dc5e5ac030f775d81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906169"
---
# <a name="imemoryallocatorfree-method"></a>IMemoryAllocator :: Free, méthode

La méthode **Free** libère la mémoire allouée par la méthode [**allocate**](imemoryallocator-allocate.md) .

## <a name="syntax"></a>Syntaxe


```C++
virtual void Free(
   void* pv
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*va* 
</dt> <dd>

Pointeur vers la mémoire à libérer.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| Bibliothèque<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |



 

 





