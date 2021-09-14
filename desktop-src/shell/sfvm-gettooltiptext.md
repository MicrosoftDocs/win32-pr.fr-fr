---
description: 'Permet à l’objet de rappel de spécifier une chaîne de texte d’info-bulle pour les éléments de menu ou les boutons de barre d’outils. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
ms.assetid: 29849218-0d30-4412-86c8-5d320bc5dd26
title: Message SFVM_GETTOOLTIPTEXT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffea70f6051ec435e14640ac70d2e9617b11305
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231197"
---
# <a name="sfvm_gettooltiptext-message"></a>\_Message SFVM GETTOOLTIPTEXT

Permet à l’objet de rappel de spécifier une chaîne de texte d’info-bulle pour les éléments de menu ou les boutons de barre d’outils. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETTOOLTIPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*idCmd \_ cchMax* \[ dans\]
</dt> <dd>

Le mot de poids faible de ce paramètre contient l’ID de commande. Le mot de poids fort contient le nombre de caractères dans la mémoire tampon *pszText* .

</dd> <dt>

*pszText* \[ à\]
</dt> <dd>

Chaîne terminée par le caractère null qui contient le texte d’aide.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
