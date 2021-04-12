---
title: IMemoryAllocator, classe
description: Implémenté par l’allocateur de mémoire pour la fonction StgConvertPropertyToVariant.
ms.assetid: a0735b62-5ed3-42df-a320-b58c742645a8
keywords:
- Stockage structuré de la classe IMemoryAllocator
- Stockage structuré de la classe IMemoryAllocator, Description
topic_type:
- apiref
api_name:
- IMemoryAllocator
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421162fd0ee6228f1dbae03eeb52e5643b0e0b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384764"
---
# <a name="imemoryallocator-class"></a>IMemoryAllocator, classe

La classe **IMemoryAllocator** est implémentée par l’allocateur de mémoire pour la fonction [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) .

## <a name="methods"></a>Méthodes



| Nom                                                     | Description                                                                                                                                                                                                        |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Lui**](imemoryallocator-allocate.md)<br/> | Alloue de la mémoire pour la fonction [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) lorsque la fonction convertit un type de données **SERIALIZEDPROPERTYVALUE** en un type de données **PROPVARIANT** .<br/> |
| [**Gratuit**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize)<br/>        | Libère la mémoire allouée par la méthode [**allocate**](imemoryallocator-allocate.md) .<br/>                                                                                                                 |



 

## <a name="remarks"></a>Notes

Cette classe est utilisée uniquement par la fonction [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| Bibliothèque<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |



 

