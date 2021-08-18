---
description: 'Avertit l’objet de rappel qu’une de ses commandes de menu ou de barre d’outils a été appelée par l’utilisateur. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
ms.assetid: 6b9e4a4d-ec45-489c-bbff-d123d5756b75
title: Message SFVM_INVOKECOMMAND (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b33eba78e0680fe940569c7a7ccfb4a27c61c3ffcb6eead0f2ff6436ec74f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968648"
---
# <a name="sfvm_invokecommand-message"></a>\_Message SFVM commande InvokeCommand

Avertit l’objet de rappel qu’une de ses commandes de menu ou de barre d’outils a été appelée par l’utilisateur. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_INVOKECOMMAND 

    wParam = (WPARAM)(UINT) idCmd;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*idCmd* \[ dans\]
</dt> <dd>

ID de commande de la barre d’outils ou de l’élément de menu sélectionné.

</dd> </dl>

## <a name="remarks"></a>Remarques

Ce message sert essentiellement la même fonction qu’un message de [**\_ commande WM**](../menurc/wm-command.md) dans une procédure de fenêtre conventionnelle. elle permet à l’objet de rappel de gérer tous les éléments qu’il a ajoutés à l’outil ou à la barre de menus de l’explorateur de Windows.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
