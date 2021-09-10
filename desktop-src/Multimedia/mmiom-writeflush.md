---
title: Message MMIOM_WRITEFLUSH (mmsystem. h)
description: Le \_ message MMIOM WRITEFLUSH est envoyé à une procédure d’e/s par la fonction mmioWrite pour demander que les données soient écrites dans un fichier ouvert et que les mémoires tampons internes utilisées par la procédure d’e/s soient vidées sur le disque.
ms.assetid: e04acaef-9584-410c-a020-af09fb888490
keywords:
- message MMIOM_WRITEFLUSH Windows Multimedia
topic_type:
- apiref
api_name:
- MMIOM_WRITEFLUSH
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b294d4c461970a3304f09088cf63a6564acd50c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364568"
---
# <a name="mmiom_writeflush-message"></a>\_Message MMIOM WRITEFLUSH

Le message **MMIOM \_ WRITEFLUSH** est envoyé à une procédure d’e/s par la fonction [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) pour demander que les données soient écrites dans un fichier ouvert et que les mémoires tampons internes utilisées par la procédure d’e/s soient vidées sur le disque.


```C++
MMIOM_WRITEFLUSH 
lParam1 = (LPARAM) lpBuffer 
lParam2 = (LPARAM) cbWrite 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*
</dt> <dd>

Pointeur vers une mémoire tampon contenant les données à écrire dans le fichier.

</dd> <dt>

<span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*
</dt> <dd>

Nombre d’octets à écrire dans le fichier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne le nombre d’octets réellement écrits dans le fichier. En cas d’erreur, la valeur de retour est 1.

## <a name="remarks"></a>Remarques

La procédure d’e/s est responsable de la mise à jour du membre **lDiskOffset** de la structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) pour refléter la nouvelle position de fichier après l’opération d’écriture.

Ce message est équivalent au message [**d' \_ écriture MMIOM**](mmiom-write.md) , à ceci près qu’il demande que la procédure d’e/s vide ses mémoires tampons internes, le cas échéant. À moins qu’une procédure d’e/s effectue une mise en mémoire tampon interne, ce message peut être géré exactement comme le message d' **\_ écriture MMIOM** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Mmsystem. h (inclure Windows. h)</dt> </dl> |



 

