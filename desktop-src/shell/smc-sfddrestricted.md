---
description: Demande s’il est acceptable de supprimer un objet de données sur l’élément spécifié par la structure SMDATA associée.
ms.assetid: 777bbc7e-6b0f-4627-9d92-4aa8209082ca
title: Message SMC_SFDDRESTRICTED (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ae6a852fd342e67edf42429f31eb7e1ba3b566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973446"
---
# <a name="smc_sfddrestricted-message"></a>\_Message SMC SFDDRESTRICTED

Demande s’il est acceptable de supprimer un objet de données sur l’élément spécifié par la structure [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) associée.


```C++
SMC_SFDDRESTRICTED 
    wParam = (WPARAM) (void **) pDropTarget
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDropTarget* 
</dt> <dd>

Adresse d’un pointeur void qui reçoit un pointeur vers votre interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . Définissez cette valeur sur **null** si vous ne souhaitez pas accepter l’objet de données.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

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



 

 
