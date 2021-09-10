---
title: Message MMIOM_RENAME (mmsystem. h)
description: Le \_ message MMIOM Rename est envoyé à une procédure d’e/s par la fonction mmioRename pour demander que le fichier spécifié soit renommé.
ms.assetid: 38a746c8-3a6f-4cb2-a5b4-c11bd1e73c8a
keywords:
- message MMIOM_RENAME Windows Multimedia
topic_type:
- apiref
api_name:
- MMIOM_RENAME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71770dec6a92693a50e8e0210da3f9b8028587c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364564"
---
# <a name="mmiom_rename-message"></a>MMIOM \_ REnommer le message

Le message **MMIOM \_ Rename** est envoyé à une procédure d’e/s par la fonction [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) pour demander que le fichier spécifié soit renommé.


```C++
MMIOM_RENAME 
lParam1 = (LPARAM) lpszOldFilename 
lParam2 = (LPARAM) lpszNewFilename 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszOldFilename*
</dt> <dd>

Pointeur vers une chaîne contenant le nom du fichier à renommer.

</dd> <dt>

<span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*lpszNewFilename*
</dt> <dd>

Pointeur vers une chaîne contenant le nouveau nom de fichier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Si le fichier est correctement renommé, la valeur de retour est zéro. Si le fichier spécifié est introuvable, la valeur de retour est MMIOERR \_ FILENOTFOUND.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Mmsystem. h (inclure Windows. h)</dt> </dl> |



 

