---
description: 'permet à l’objet de rappel de fusionner les éléments de menu dans les menus de l’explorateur de Windows. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_MERGEMENU (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59bb99a3-9a5a-4ea5-9830-b04d7d886b3f
api_name:
- SFVM_MERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5cf95a7576c15ab1c3e64ebe55e244feffa6d86d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293335"
---
# <a name="sfvm_mergemenu-message"></a>\_Message SFVM MERGEMENU

permet à l’objet de rappel de fusionner les éléments de menu dans les menus de l’explorateur de Windows. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_MERGEMENU 

    lParam = (LPARAM)(LPQCMINFO) pInfo;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pinfo* \[ à\]
</dt> <dd>

Structure [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) contenant les informations nécessaires pour fusionner les éléments dans le menu.

</dd> </dl>

## <a name="remarks"></a>Notes

Ce message remplit essentiellement les mêmes fonctions que [**IShellBrowser :: InsertMenusSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) et [**IShellBrowser :: SetMenuSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) dans un affichage de dossier personnalisé. pour plus d’informations, consultez la section *utilisation de IShellBrowser pour communiquer avec Windows Explorer* dans [implémentation d’un affichage des dossiers](../lwef/nse-folderview.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
