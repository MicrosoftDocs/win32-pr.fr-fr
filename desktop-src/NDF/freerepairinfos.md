---
title: FreeRepairInfos, fonction (Ndattributils. h)
description: Libère la mémoire allouée en interne à un tableau de structures RepairInfo.
ms.assetid: c40f9d10-8d9e-4c79-ac0b-fa88608888f1
keywords:
- FreeRepairInfos fonction NDF
topic_type:
- apiref
api_name:
- FreeRepairInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63bf6ab2154376302e4c9dd076ccaf83a0c565c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103288"
---
# <a name="freerepairinfos-function"></a>FreeRepairInfos fonction)

La fonction **FreeRepairInfos** libère la mémoire allouée en interne à un tableau de structures [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) . Cette fonction appelle [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer de la mémoire.

## <a name="syntax"></a>Syntaxe


```C++
VOID FreeRepairInfos(
  _In_ RepairInfo *pInfo,
       ULONG      RepairCount,
       BOOL       bFreePointer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pinfo* \[ dans\]
</dt> <dd>

Tapez : **[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _

Tableau de structures. La mémoire allouée pointée par ces structures sera libérée.

</dd> <dt>

_RepairCount * 
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

