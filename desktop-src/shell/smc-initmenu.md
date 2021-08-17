---
description: Vous informe de l’initialisation de la bande de menu.
title: Message SMC_INITMENU (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 415ee805-2b57-4f8f-85d9-2b38cd05998d
api_name:
- SMC_INITMENU
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f354769ca18c7490e8bcbf9b1aec0d6c30eb2503dfd66c8a9761a2dddf8ad13d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968058"
---
# <a name="smc_initmenu-message"></a>\_Message SMC INITMENU

Vous informe de l’initialisation de la bande de menu.


```C++
SMC_INITMENU
            
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



 

 




