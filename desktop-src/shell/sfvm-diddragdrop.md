---
description: SFVM \_ DIDDRAGDROP peut être modifié ou non disponible.
ms.assetid: 5d37cf61-d8a7-4afa-9159-fea13d2b1d59
title: Message SFVM_DIDDRAGDROP (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025bcf6320b014ff31b0819f394dd8b76fa90e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991681"
---
# <a name="sfvm_diddragdrop-message"></a>\_Message SFVM DIDDRAGDROP

\[**SFVM \_ DIDDRAGDROP** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]

Notifie la fonction de rappel qu’une opération de glisser-déplacer a commencé. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_DIDDRAGDROP 
    wParam = (WPARAM)(DWORD) dwEffect;
    lParam = (LPARAM)(IDataObject*) pIdo;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwEffect* \[ dans\]
</dt> <dd>

Spécificateur d’effet de déplacement de l’énumération [**DROPEFFECT**](../com/dropeffect-constants.md) . Cela est obtenu en appelant [**SHDoDragDrop**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop).

</dd> <dt>

*pIdo* \[ dans\]
</dt> <dd>

Pointeur vers l’instance [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) .

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                |
| Fin de la prise en charge des clients<br/>    | Windows XP SP2<br/>                                                      |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
