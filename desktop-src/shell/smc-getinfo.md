---
description: Demande des informations sur un élément de menu normal.
title: Message SMC_GETINFO (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 07f35a64-eff0-48e8-a2fc-719ccf1eca18
api_name:
- SMC_GETINFO
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 95f27905a59fd8ce7c84cfc1166b59cb38356934b3603b0cec7f56c2365a3984
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968108"
---
# <a name="smc_getinfo-message"></a>\_Message SMC GETINFO

Demande des informations sur un élément de menu normal.


```C++
SMC_GETINFO 
    lParam = (LPARAM) (LPSMINFO) psminfo
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*psminfo* 
</dt> <dd>

Pointeur vers une structure [**SMINFO**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) . Remplissez la structure avec les informations appropriées et renvoyez \_ OK.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>ShObjIdl. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



 

 




