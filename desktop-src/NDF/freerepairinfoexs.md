---
title: FreeRepairInfoExs, fonction (Ndattributils. h)
description: Libère la mémoire allouée en interne à un tableau de structures RepairInfoEx.
ms.assetid: b4e3e758-88cd-4ce2-b1a4-5b47889aae9b
keywords:
- FreeRepairInfoExs fonction NDF
topic_type:
- apiref
api_name:
- FreeRepairInfoExs
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 094c745486526caa870a500019de3aa819b6fe5a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110498"
---
# <a name="freerepairinfoexs-function"></a>FreeRepairInfoExs fonction)

La fonction **FreeRepairInfoExs** libère la mémoire allouée en interne à un tableau de structures [**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) . Cette fonction appelle [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer de la mémoire.

## <a name="syntax"></a>Syntaxe


```C++
VOID FreeRepairInfoExs(
  _In_ RepairInfoEx *pInfo,
       ULONG        RepairCount,
       BOOL         bFreePointer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pinfo* \[ dans\]
</dt> <dd>

Type : **[ **RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)\***

Tableau de structures. La mémoire allouée pointée par ces structures sera libérée.

</dd> <dt>

*RepairCount* 
</dt> <dd>

Type : **ULong**

Nombre de structures dans le tableau pointé par *pinfo*.

</dd> <dt>

*bFreePointer* 
</dt> <dd>

Type : **bool**

True si le tableau de structures doit également être supprimé ; Sinon, false.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

