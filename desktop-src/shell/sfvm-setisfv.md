---
description: 'Avertit l’objet de rappel du site de conteneur. Utilisé uniquement quand IObjectWithSite :: SetSite n’est pas pris en charge et SHCreateShellFolderViewEx est utilisé. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
ms.assetid: a4aa40f8-1d98-4686-86e2-87280e470aac
title: Message SFVM_SETISFV (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83021f1d6d52286f08e8ec7bd51bbaa806c17c7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973811"
---
# <a name="sfvm_setisfv-message"></a>\_Message SFVM SETISFV

\[Cette notification est prise en charge via Windows XP Service Pack 2 (SP2) et Windows Server 2003. Il est possible qu’il ne soit pas pris en charge dans les versions ultérieures de Windows.\]

Avertit l’objet de rappel du site de conteneur. Utilisé uniquement quand [**IObjectWithSite :: SetSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) n’est pas pris en charge et [**SHCreateShellFolderViewEx**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) est utilisé. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_SETISFV
    lParam = (LPARAM)(IUnknown*) site;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*site* \[ dans\]
</dt> <dd>

Pointeur vers l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) du site conteneur.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
