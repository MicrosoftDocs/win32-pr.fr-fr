---
title: HWINEVENTHOOK (WINDEF. h)
description: Utilisé pour déclarer une fonction de raccordement d’événement de fenêtre.
ms.assetid: fa193e8e-46a8-46d4-83e1-e6274276b218
keywords:
- HWINEVENTHOOK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf526846916dfdd701f4f5ee98778dbbe9e66d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509106"
---
# <a name="hwineventhook"></a>HWINEVENTHOOK

Utilisé pour déclarer une fonction de raccordement d’événement de fenêtre.


```C++
typedef HANDLE HWINEVENTHOOK;
```



## <a name="remarks"></a>Notes

Ce type de données est utilisé avec la fonction de rappel [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) et les fonctions [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) et [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                                          |
| Composant redistribuable<br/>          | Active Accessibility 1,3 RDK sur Windows NT 4,0 avec SP6 et versions ultérieures et Windows 95<br/>                                   |
| En-tête<br/>                   | <dl> <dt>WINDEF. h (WINVER >= 0x0500) (inclure Windows. h)</dt> </dl> |



 

 





