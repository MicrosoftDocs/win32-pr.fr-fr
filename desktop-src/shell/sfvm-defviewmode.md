---
description: 'Permet à l’objet de rappel de spécifier le mode d’affichage. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_DEFVIEWMODE (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5118fc81-490f-4d76-9361-0d6af0c4b4c0
api_name:
- SFVM_DEFVIEWMODE
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 28958fd992f70924ebbd51c06090d3a55c0ef8e6418d1ee055c5eb534acb9d3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090159"
---
# <a name="sfvm_defviewmode-message"></a>\_Message SFVM DEFVIEWMODE

Permet à l’objet de rappel de spécifier le mode d’affichage. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_DEFVIEWMODE 

    lParam = (LPARAM)(FOLDERVIEWMODE*) pViewMode;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pViewMode* \[ à\]
</dt> <dd>

L’une des valeurs du type énuméré [**FOLDERVIEWMODE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode) .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
