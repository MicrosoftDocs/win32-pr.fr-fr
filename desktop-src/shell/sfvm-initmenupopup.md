---
description: 'permet à l’objet de rappel de modifier un menu contextuel Windows Explorer avant qu’il ne soit affiché. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_INITMENUPOPUP (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9d7e96e9-c52e-43bd-945b-05db33c8dfd0
api_name:
- SFVM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: fd69d19f753c1c72c1e0c143a0aface2cdb234cb2ace8c87d559834b97bbf0f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592315"
---
# <a name="sfvm_initmenupopup-message"></a>\_Message SFVM INITMENUPOPUP

permet à l’objet de rappel de modifier un menu contextuel Windows Explorer avant qu’il ne soit affiché. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_INITMENUPOPUP 

    wParam = (WPARAM)(int) idCmd,nIndex;

    lParam = (LPARAM)(HMENU) hmenu;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*idCmd \_ nIndex* \[ dans\]
</dt> <dd>

Le mot de poids faible de ce paramètre contient la valeur du premier ID de commande réservé pour les commandes du client. Le mot de poids fort contient l’index du menu.

</dd> <dt>

*HMENU* \[ in, out\]
</dt> <dd>

Handle du menu.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’objet de vue de dossier système envoie ce message lorsqu’un menu est sélectionné, mais avant son affichage. Traiter ce message si, par exemple, vous devez activer ou désactiver les commandes de menu. Le menu contextuel peut être :

-   Le menu fichier, modifier ou afficher.
-   Menu de niveau supérieur défini par le client.
-   Sous-menu défini par le client.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SFVM \_ MERGEMENU**](sfvm-mergemenu.md)
</dt> </dl>

 

 
