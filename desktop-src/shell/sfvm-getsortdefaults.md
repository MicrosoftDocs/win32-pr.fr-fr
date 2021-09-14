---
description: 'Permet à l’objet de rappel de spécifier un paramètre de tri par défaut. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_GETSORTDEFAULTS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: edd428f2-50d9-4819-ba77-df51262e33ff
api_name:
- SFVM_GETSORTDEFAULTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: db6477cc9660f8084e2bf8298e028ed7a445f26c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231203"
---
# <a name="sfvm_getsortdefaults-message"></a>\_Message SFVM GETSORTDEFAULTS

Permet à l’objet de rappel de spécifier un paramètre de tri par défaut. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETSORTDEFAULTS 

    wParam = (WPARAM)(int*) iDirection;

    lParam = (LPARAM)(int*) iColumn;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*iDirection* \[ à\]
</dt> <dd>

Sens de tri par défaut. Définissez ce paramètre sur une valeur positive pour effectuer un tri dans l’ordre croissant. Définissez ce paramètre sur zéro ou sur une valeur négative pour effectuer un tri dans l’ordre décroissant.

</dd> <dt>

*IColumn* \[ à\]
</dt> <dd>

Colonne utilisée pour le tri. Ce sera passé à [**IShellFolder :: CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) dans les 16 bits inférieurs de sa valeur *lParam* .

</dd> </dl>

## <a name="remarks"></a>Notes

> [!Note]  
> : **SFVM \_ GETSORTDEFAULTS** n’est pas reconnu par l’objet de vue de dossier système.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
