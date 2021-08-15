---
description: Demande le titre et le texte d’une info-bulle de Chevron pour l’élément spécifié par la structure SMDATA associée.
ms.assetid: 7bce4079-994c-4eb0-ab86-9044701d85a1
title: Message SMC_CHEVRONGETTIP (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e64636994743d4b13a96fe75947fb515c4dbd3edcc94e6dee0fa85efb8bc9d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968238"
---
# <a name="smc_chevrongettip-message"></a>\_Message SMC CHEVRONGETTIP

Demande le titre et le texte d’une info-bulle de Chevron pour l’élément spécifié par la structure [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) associée.


```C++
SMC_CHEVRONGETTIP 
    wParam = (WPARAM) (LPWSTR) pwszTipTitle;
    lParam = (LPARAM) (LPWSTR) pwszTipText
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pwszTipTitle* 
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit une chaîne Unicode terminée par le caractère **null** qui contient le titre de l’info-bulle. Cette chaîne ne doit pas dépasser la longueur maximale de \_ caractères de chemin d’accès, y compris le caractère **null** de fin.

</dd> <dt>

*pwszTipText* 
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit une chaîne Unicode terminée par le caractère **null** qui contient le texte de l’info-bulle. Cette chaîne ne doit pas dépasser la longueur maximale de \_ caractères de chemin d’accès, y compris le caractère **null** de fin.

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



 

 




