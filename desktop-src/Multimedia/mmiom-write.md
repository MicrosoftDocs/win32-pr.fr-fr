---
title: Message MMIOM_WRITE (mmsystem. h)
description: Le \_ message d’écriture MMIOM est envoyé à une procédure d’e/s par la fonction mmioWrite pour demander l’écriture des données dans un fichier ouvert.
ms.assetid: 46e2dd9a-c4a7-4c99-86e4-a67b424411d1
keywords:
- Message MMIOM_WRITE Windows Multimedia
topic_type:
- apiref
api_name:
- MMIOM_WRITE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27cf96827f803608c369cc9022faa6235add9ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942745"
---
# <a name="mmiom_write-message"></a>MMIOM \_ écrire un message

Le message d' **\_ écriture MMIOM** est envoyé à une procédure d’e/s par la fonction [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) pour demander l’écriture des données dans un fichier ouvert.


```C++
MMIOM_WRITE 
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

## <a name="remarks"></a>Notes

La procédure d’e/s est responsable de la mise à jour du membre **lDiskOffset** de la structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) pour refléter la nouvelle position de fichier après l’opération d’écriture.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>MMSYSTEM. h (inclure Windows. h)</dt> </dl> |



 

