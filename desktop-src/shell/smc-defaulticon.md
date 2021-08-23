---
description: Retourne l’icône par défaut pour l’élément spécifié par la structure SMDATA associée.
title: Message SMC_DEFAULTICON (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d5f6789a-f160-4fba-ba64-b1a0c491fdaa
api_name:
- SMC_DEFAULTICON
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c0245cad585f461fbc1b22611b0a39a25ec0e6ac235bb29a490fdd47ba5e5979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968198"
---
# <a name="smc_defaulticon-message"></a>\_Message SMC DEFAULTICON

Retourne l’icône par défaut pour l’élément spécifié par la structure [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) associée.


```C++
SMC_DEFAULTICON 
    wParam = (WPARAM) (LPWSTR) pwszIcon;
    lParam = (LPARAM) (int) iIcon
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pwszIcon* 
</dt> <dd>

Pointeur vers une chaîne qui reçoit le chemin d’accès qualifié complet du fichier qui contient l’icône par défaut.

</dd> <dt>

*Icône* 
</dt> <dd>

Pointeur vers un entier qui reçoit l’index de l’icône dans le fichier spécifié par *pwszIcon*.

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



 

 




