---
description: Vous avertit qu’une info-bulle est sur le point d’être affichée pour le Chevron associé à l’élément spécifié par la structure SMDATA qui l’accompagne.
title: Message SMC_DISPLAYCHEVRONTIP (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: e4ec4839-e49a-4563-9bc9-79f9d4d54658
api_name:
- SMC_DISPLAYCHEVRONTIP
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f1107af5cd621bafbc1e463101cee2ea57236b9d29844d6183963134b50ce3ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968168"
---
# <a name="smc_displaychevrontip-message"></a>\_Message SMC DISPLAYCHEVRONTIP

Vous avertit qu’une info-bulle est sur le point d’être affichée pour le Chevron associé à l’élément spécifié par la structure [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) qui l’accompagne.


```C++
SMC_DISPLAYCHEVRONTIP
            
```



## <a name="parameters"></a>Paramètres

Ce message n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Return \_ OK pour afficher l’info-bulle. Retourne \_ la valeur false pour empêcher l’affichage de l’info-bulle.

## <a name="remarks"></a>Remarques

Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>ShObjIdl. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



 

 




