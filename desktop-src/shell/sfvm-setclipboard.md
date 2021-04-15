---
description: Notifie le IShellView quand l’un de ses objets est placé dans le presse-papiers à la suite d’une commande de menu. Utilisé par le \_ message SHShellFolderView.
title: Message SFVM_SETCLIPBOARD (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6a4cf0c5-2349-4e1e-b6c5-ee9b5430456e
api_name:
- SFVM_SETCLIPBOARD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c9c30848de77ef7de101eaa9d724f2f26f9d384c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991801"
---
# <a name="sfvm_setclipboard-message"></a>\_Message SFVM SETCLIPBOARD

Notifie le [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) quand l’un de ses objets est placé dans le presse-papiers à la suite d’une commande de menu. Utilisé par [**le \_ message SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_SETCLIPBOARD 

    lParam = (DWORD) dwEffect;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwEffect* \[ dans\]
</dt> <dd>

Utilisez (WPARAM)-2 si l’élément est coupé dans le presse-papiers ou (WPARAM)-3 Si l’élément est copié dans le presse-papiers.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




