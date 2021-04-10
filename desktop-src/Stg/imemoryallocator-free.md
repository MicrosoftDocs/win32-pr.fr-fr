---
title: Méthode IMemoryAllocator Free
description: La méthode Free libère la mémoire allouée par la méthode Allocate.
ms.assetid: 41f81cba-4431-4ff7-ac84-8ff5bea71b65
keywords:
- Stockage structuré de méthode libre
- Free, méthode stockage structuré, interface IMemoryAllocator
- Stockage structuré de l’interface IMemoryAllocator, méthode libre
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
ms.openlocfilehash: 7c07731f60aba7d847c79467b2b2c166b363d807
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032458"
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



 

 





