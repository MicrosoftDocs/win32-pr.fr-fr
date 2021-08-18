---
description: Vous avertit qu’une bande de menu a été créée.
title: Message SMC_CREATE (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8eeca6f6-1718-4ff6-b4a7-4b68b9527468
api_name:
- SMC_CREATE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 537c535d5470a691cf110b2217bb31cbfd0ad78b328f4fbb32a1445e0c5e6597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968218"
---
# <a name="smc_create-message"></a>\_Créer un message SMC

Vous avertit qu’une bande de menu a été créée.


```C++
SMC_CREATE 
    lParam = (LPARAM) (LPSMDATA) psmd
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*psmd* 
</dt> <dd>

Pointeur vers le membre **pvUserData** d’une structure [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .

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



 

 




