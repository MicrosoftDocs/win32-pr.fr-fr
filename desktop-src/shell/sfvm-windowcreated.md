---
description: 'Avertit l’objet de rappel que la fenêtre d’affichage des dossiers est en cours de création. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_WINDOWCREATED (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b57eb1d8-a897-4358-a855-89e152035eff
api_name:
- SFVM_WINDOWCREATED
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2d09957e1164d5caacbddc23c9a72cb33ef80ffa156dd0538c0be1e24f192018
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111159"
---
# <a name="sfvm_windowcreated-message"></a>\_Message SFVM WINDOWCREATED

Avertit l’objet de rappel que la fenêtre d’affichage des dossiers est en cours de création. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_WINDOWCREATED 

    wParam = (WPARAM)(HWND) hwndView;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hwndView* \[ dans\]
</dt> <dd>

Handle de fenêtre de la vue du dossier.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
