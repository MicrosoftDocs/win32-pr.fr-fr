---
description: 'Permet à l’objet de rappel d’ajouter des boutons à la barre d’outils. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_GETBUTTONINFO (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 983652ed-7309-46aa-a6c9-7516411ba5ac
api_name:
- SFVM_GETBUTTONINFO
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d0db40f7c1f54cd13d54765ba34a8eab31246809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973486"
---
# <a name="sfvm_getbuttoninfo-message"></a>\_Message SFVM GETBUTTONINFO

Permet à l’objet de rappel d’ajouter des boutons à la barre d’outils. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETBUTTONINFO 

    lParam = (LPARAM)(LPTBINFO) ptbinfo;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ptbinfo* \[ à\]
</dt> <dd>

Adresse d’une structure [**TBINFO**](/windows/desktop/api/Shlobj/ns-shlobj-tbinfo) qui spécifie le nombre de boutons et la façon dont ils doivent être ajoutés à la barre d’outils.

</dd> </dl>

## <a name="remarks"></a>Notes

Les boutons peuvent être ajoutés aux boutons de l’objet d’affichage des dossiers système standard ou être ajoutés à la place des boutons standard. Ce message est suivi d’un message [**SFVM \_ GETBUTTONS**](sfvm-getbuttons.md) qui extrait les informations relatives aux spécificités du bouton.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
