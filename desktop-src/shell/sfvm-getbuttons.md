---
description: 'Permet à l’objet de rappel de spécifier les boutons à ajouter à la barre d’outils. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
ms.assetid: 0c0dbf61-9da9-4bcc-bad9-92c3f78db78f
title: Message SFVM_GETBUTTONS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299641ef45d17a6ad1e4d709c3250abe220e297daedabcb563eeba9dcf56262a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008979"
---
# <a name="sfvm_getbuttons-message"></a>\_Message SFVM GETBUTTONS

Permet à l’objet de rappel de spécifier les boutons à ajouter à la barre d’outils. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETBUTTONS 

    wParam = (WPARAM)(DWORD) idCmdFirst,cbtnMax;

    lParam = (LPARAM)(LPTBBUTTON) pbtn;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*idCmdFirst \_ cbtnMax* \[ dans\]
</dt> <dd>

Contient les valeurs 2 16 bits compressées dans le paramètre avec la macro [**MAKEWPARAM**](/windows/win32/api/winuser/nf-winuser-makewparam) . Le mot de poids faible contient l’ID de commande initial. Le mot de poids fort contient le nombre de boutons à ajouter, comme spécifié dans le message [**\_ GETBUTTONINFO SFVM**](sfvm-getbuttoninfo.md) précédent.

</dd> <dt>

*pbtn* \[ à\]
</dt> <dd>

Adresse d’un tableau de structures [**TBBUTTON**](/windows/win32/api/commctrl/ns-commctrl-tbbutton) , une pour chaque bouton à ajouter à la barre d’outils.

</dd> </dl>

## <a name="remarks"></a>Remarques

Ce message est précédé d’un message [**SFVM \_ GETBUTTONINFO**](sfvm-getbuttoninfo.md) . L’objet de rappel doit gérer ce message pour spécifier le nombre de boutons et l’emplacement où ils doivent être placés dans la barre d’outils. En fonction de la façon dont l’objet de rappel répond au message **SFVM \_ GETBUTTONINFO** , les boutons spécifiés par le paramètre *pbtn* seront ajoutés ou ajoutés aux boutons standard de l’objet d’affichage des dossiers système ou remplacent le jeu standard.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
