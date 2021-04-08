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
ms.openlocfilehash: 7a24d15ec5a8a69b3c8c40700273ebcb6f32bcfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941909"
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

Tapez : **[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _

Structure à mettre à jour.

</dd> <dt>

_Source * \[ dans\]
</dt> <dd>

Type : **const [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _

Structure existante à copier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *HRESULT**

Les valeurs de retour possibles incluent, mais ne sont pas limitées à, les éléments suivants.



| Code de retour                                                                                   | Description                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | L’opération a réussi.<br/>                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Un ou plusieurs paramètres n’ont pas été fournis correctement.<br/>          |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour terminer cette opération.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> </dl>

 

 





