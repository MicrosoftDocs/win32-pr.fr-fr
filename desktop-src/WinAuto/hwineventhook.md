---
title: HWINEVENTHOOK (WINDEF. h)
description: Utilisé pour déclarer une fonction de raccordement d’événement de fenêtre.
ms.assetid: fa193e8e-46a8-46d4-83e1-e6274276b218
keywords:
- HWINEVENTHOOK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf526846916dfdd701f4f5ee98778dbbe9e66d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127191715"
---
# <a name="hwineventhook"></a>HWINEVENTHOOK

Utilisé pour déclarer une fonction de raccordement d’événement de fenêtre.


```C++
typedef HANDLE HWINEVENTHOOK;
```



## <a name="remarks"></a>Notes

Ce type de données est utilisé avec la fonction de rappel [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) et les fonctions [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) et [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                                          |
| Composant redistribuable<br/>          | Active Accessibility 1,3 RDK sur Windows NT 4,0 avec SP6 et versions ultérieures et Windows 95<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Windef. h (WINVER >= 0x0500) (inclure Windows. h)</dt> </dl> |



 

 





