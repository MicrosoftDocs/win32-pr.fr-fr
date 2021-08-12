---
title: CopyRepairInfo, fonction (Ndattributils. h)
description: Crée une copie d’une structure RepairInfo.
ms.assetid: a1147ce6-9a90-4a46-8fe4-da3353391a13
keywords:
- CopyRepairInfo fonction NDF
topic_type:
- apiref
api_name:
- CopyRepairInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e40a054df2b16684840f22295f0c26de6029ef150a97ca8839c98d94713ab030
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620434"
---
# <a name="copyrepairinfo-function"></a>CopyRepairInfo fonction)

La fonction **CopyRepairInfo** crée une copie d’une structure [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CopyRepairInfo(
  _Out_       RepairInfo *Dest,
  _In_  const RepairInfo *Source
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Dest* \[ . à\]
</dt> <dd>

Type : **[ **RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\***

Structure à mettre à jour.

</dd> <dt>

*Source* \[ dans\]
</dt> <dd>

Type : **const [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \***

Structure existante à copier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Les valeurs de retour possibles incluent, mais ne sont pas limitées à, les éléments suivants.



| Code de retour                                                                                   | Description                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | L’opération a réussi.<br/>                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Un ou plusieurs paramètres n’ont pas été fournis correctement.<br/>          |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour terminer cette opération.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> </dl>

 

 





