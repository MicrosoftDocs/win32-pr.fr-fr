---
title: Message MMIOM_READ (mmsystem. h)
description: Le \_ message de lecture MMIOM est envoyé à une procédure d’e/s par la fonction mmioRead pour demander qu’un nombre spécifié d’octets soit lu à partir d’un fichier ouvert.
ms.assetid: db769a68-f0ac-4a79-931e-6174e438439d
keywords:
- message MMIOM_READ Windows Multimedia
topic_type:
- apiref
api_name:
- MMIOM_READ
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcf5bbdbb20e2bc168f93857a7d59016197ccc4142d4ba18a2e6fd80842ff06c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065349"
---
# <a name="mmiom_read-message"></a>MMIOM \_ lire le message

Le message de **\_ lecture MMIOM** est envoyé à une procédure d’e/s par la fonction [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) pour demander qu’un nombre spécifié d’octets soit lu à partir d’un fichier ouvert.


```C++
MMIOM_READ 
lParam1 = (LPARAM) lBuffer 
lParam2 = (LPARAM) cbRead 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lBuffer"></span><span id="lbuffer"></span><span id="LBUFFER"></span>*lBuffer*
</dt> <dd>

Pointeur vers la mémoire tampon à remplir avec les données lues à partir du fichier.

</dd> <dt>

<span id="cbRead"></span><span id="cbread"></span><span id="CBREAD"></span>*cbRead*
</dt> <dd>

Nombre d’octets à lire à partir du fichier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne le nombre d’octets réellement lus à partir du fichier. Si le nombre d’octets ne peut pas être lu, la valeur de retour est 0. En cas d’erreur, la valeur de retour est 1.

## <a name="remarks"></a>Remarques

La procédure d’e/s est responsable de la mise à jour du membre **lDiskOffset** de la structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) pour refléter la nouvelle position de fichier après l’opération de lecture.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Mmsystem. h (inclure Windows. h)</dt> </dl> |



 

