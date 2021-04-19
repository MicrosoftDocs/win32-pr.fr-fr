---
title: IMemoryAllocator Allocate, méthode
description: La méthode Allocate alloue de la mémoire pour la fonction StgConvertPropertyToVariant lorsque la fonction convertit un type de données SERIALIZEDPROPERTYVALUE en un type de données PROPVARIANT.
ms.assetid: aa9c9308-fb55-405c-901a-9d5abfac5395
keywords:
- Allouer une méthode stockage structuré
- Allouer une méthode stockage structuré, interface IMemoryAllocator
- Stockage structuré de l’interface IMemoryAllocator, méthode Allocate
topic_type:
- apiref
api_name:
- IMemoryAllocator.Allocate
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ee4b220e1c1e14ceed685e9b2adc694a44d2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106532044"
---
# <a name="imemoryallocatorallocate-method"></a>IMemoryAllocator :: Allocate, méthode

La méthode **allocate** alloue de la mémoire pour la fonction [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) lorsque la fonction convertit un type de données **SERIALIZEDPROPERTYVALUE** en un type de données **PROPVARIANT** .

## <a name="syntax"></a>Syntaxe


```C++
virtual void* Allocate(
  [in] ULONG cbSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cbSize* \[ dans\]
</dt> <dd>

Spécifie la taille de la mémoire à allouer.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| Bibliothèque<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |



 

