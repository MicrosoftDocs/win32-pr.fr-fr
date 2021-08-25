---
description: SFVM \_ QUERYFSNOTIFY peut être modifié ou non disponible.
ms.assetid: 5d777115-bae3-47c4-9edc-c99c40a4f926
title: Message SFVM_QUERYFSNOTIFY (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 932650257ddb039e3841a583c3856316a86eca469db74a0e8ab6ebf33e9411f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941989"
---
# <a name="sfvm_queryfsnotify-message"></a>\_Message SFVM QUERYFSNOTIFY

\[**SFVM \_ QUERYFSNOTIFY** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]

Permet à l’objet de rappel d’inscrire un dossier afin que les modifications apportées à la vue de ce dossier génèrent des notifications. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_QUERYFSNOTIFY 
    lParam = (LPARAM)(SHChangeNotifyEntry*) shcne;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*shcne* \[ in, out\]
</dt> <dd>

Structure destinée à contenir le PIDL de l’élément pour surveiller les événements et indiquer si les sous-dossiers de cet élément doivent également être surveillés.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                |
| Fin de la prise en charge des clients<br/>    | Windows XP SP2<br/>                                                      |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
