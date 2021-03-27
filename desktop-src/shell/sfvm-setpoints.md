---
description: Définit les points des objets actuellement sélectionnés sur l’objet de données sur les commandes copier et couper. Utilisé par le \_ message SHShellFolderView.
title: Message SFVM_SETPOINTS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d2c3e06a-19e4-4b78-9b7c-1a256582786e
api_name:
- SFVM_SETPOINTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1df501f162fb19335fcf1672299a74135672db22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210831"
---
# <a name="sfvm_setpoints-message"></a>\_Message SFVM SetPoints

Définit les points des objets actuellement sélectionnés sur l’objet de données sur les commandes **copier** et **couper** . Utilisé par [**le \_ message SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_SETPOINTS 

    lParam = (LPARAM) pdtobj;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pdtobj* \[ dans\]
</dt> <dd>Pointeur vers un <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">**IDataObject**</a> des commandes **Copy** et **Cut** .</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne toujours zéro.

## <a name="remarks"></a>Notes

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
