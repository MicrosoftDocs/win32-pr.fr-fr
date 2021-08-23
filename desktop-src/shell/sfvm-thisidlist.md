---
description: SFVM \_ THISIDLIST peut être modifié ou non disponible.
ms.assetid: 488f696d-aa71-4727-bbd2-c99e7d245d85
title: Message SFVM_THISIDLIST (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd00f1cfc2b6661dac2414f0327cab03d4c0586eb62b992b5e33f81e64565246
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968628"
---
# <a name="sfvm_thisidlist-message"></a>\_Message SFVM THISIDLIST

\[**SFVM \_ THISIDLIST** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]

Permet à l’objet de rappel de spécifier le pointeur de la vue vers une liste d’identificateurs d’éléments (PIDL). Utilisé uniquement lorsque [**IPersistIDList :: SetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) et [**IPersistFolder2 :: GetCurFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) ont échoué. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_THISIDLIST
    lParam = (LPARAM)(LPITEMIDLIST*) pidl;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PIDL* \[ à\]
</dt> <dd>

Adresse du PIDL de la vue.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                |
| Fin de la prise en charge des clients<br/>    | Windows XP SP2<br/>                                                      |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
