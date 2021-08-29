---
description: 'Permet à l’objet de rappel de spécifier le nombre d’éléments dans l’affichage des dossiers. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_DEFITEMCOUNT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 62306eaa-e52e-432b-9233-d990519d5739
api_name:
- SFVM_DEFITEMCOUNT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 29e92aca1a1f52c0722c890f097ddab33255e814ec35768208644a3a9d814353
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709879"
---
# <a name="sfvm_defitemcount-message"></a>\_Message SFVM DEFITEMCOUNT

Permet à l’objet de rappel de spécifier le nombre d’éléments dans l’affichage des dossiers. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_DEFITEMCOUNT 

    lParam = (LPARAM)(UINT*) cItems;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CItems* \[ à\]
</dt> <dd>

Nombre d’éléments dans l’affichage des dossiers.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
