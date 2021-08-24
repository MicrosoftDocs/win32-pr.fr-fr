---
description: 'Avertit l’objet de rappel du site de conteneur. Utilisé uniquement quand IObjectWithSite :: SetSite n’est pas pris en charge et SHCreateShellFolderViewEx est utilisé. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
ms.assetid: a4aa40f8-1d98-4686-86e2-87280e470aac
title: Message SFVM_SETISFV (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6d9ad3e9b1b8302089da8a59a8d5502a04392da77c6fc5276725b144efa026
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660799"
---
# <a name="sfvm_setisfv-message"></a>\_Message SFVM SETISFV

\[cette notification est prise en charge par Windows XP Service Pack 2 (SP2) et Windows Server 2003. Il est possible qu’il ne soit pas pris en charge dans les versions ultérieures de Windows.\]

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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
