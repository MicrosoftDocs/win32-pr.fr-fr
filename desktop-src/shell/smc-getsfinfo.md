---
description: Demande des informations sur un élément de menu de dossier de Shell.
title: Message SMC_GETSFINFO (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4459670c-f0fd-4ae8-8a1f-810e1dcac713
api_name:
- SMC_GETSFINFO
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f3a02b61565eb08f623978900d6ce47e30eea85e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522356"
---
# <a name="smc_getsfinfo-message"></a>\_Message SMC GETSFINFO

Demande des informations sur un élément de menu de dossier de Shell.


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

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>ShObjIdl. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



 

 




