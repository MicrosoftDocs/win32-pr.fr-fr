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
ms.openlocfilehash: ff74e59d0ef445a74d1141950b2b10e79ebce5502a02ec38c446bddc7317a885
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968078"
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



 

 




