---
description: 'Avertit l’objet de rappel qu’un événement a eu lieu et affecte l’un de ses éléments. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_FSNOTIFY (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ff159c35-afdf-4147-8dd6-7febd9519b18
api_name:
- SFVM_FSNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 74c17f9d4b8c8c1979fa7da2d6f0ff63dff74a9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411469"
---
# <a name="sfvm_fsnotify-message"></a>\_Message SFVM FSNOTIFY

Avertit l’objet de rappel qu’un événement a eu lieu et affecte l’un de ses éléments. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_FSNOTIFY 

    wParam = (WPARAM)(LPCITEMIDLIST*) ppidl;

    lParam = (LPARAM)(DWORD) lEvent;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppidl* \[ dans\]
</dt> <dd>

Pointeur de PIDL de l’élément affecté.

</dd> <dt>

*lEvent* \[ dans\]
</dt> <dd>

Valeur SHCNE qui indique l’événement qui s’est produit. Pour obtenir la liste des valeurs possibles, consultez [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify).

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
