---
description: Exécutez l’élément de dossier shell spécifié dans la structure SMDATA associée.
title: Message SMC_SFEXEC (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bb8f6434-0936-460f-b7dc-39be58bb70ce
api_name:
- SMC_SFEXEC
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e4d02763745a0ffb548777c92d14ee7928a29a58d6a46ff7c335ac0300f64bd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967998"
---
# <a name="smc_sfexec-message"></a>\_Message SMC SFEXEC

Exécutez l’élément de dossier shell spécifié dans la structure [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) associée.


```C++
SMC_SFEXEC
            
```



## <a name="parameters"></a>Paramètres

Ce message n’a pas de paramètres.

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



 

 




