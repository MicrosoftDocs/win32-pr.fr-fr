---
title: Message MMIOM_SEEK (mmsystem. h)
description: Le \_ message de recherche MMIOM est envoyé à une procédure d’e/s par la fonction mmioSeek pour demander que la position actuelle du fichier soit déplacée.
ms.assetid: 428b231a-6e00-4458-9ba2-e9b0b028843a
keywords:
- Message MMIOM_SEEK Windows Multimedia
topic_type:
- apiref
api_name:
- MMIOM_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4855ec4e610f1456e1bf26ee05800e31933f05fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510781"
---
# <a name="mmiom_seek-message"></a>MMIOM le \_ message de recherche

Le message de **\_ recherche MMIOM** est envoyé à une procédure d’e/s par la fonction [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) pour demander que la position actuelle du fichier soit déplacée.


```C++
MMIOM_SEEK 
lParam1 = (LPARAM) lNewFilePos 
lParam2 = (LPARAM) lChangeFlag 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lNewFilePos"></span><span id="lnewfilepos"></span><span id="LNEWFILEPOS"></span>*lNewFilePos*
</dt> <dd>

Nouvelle position de fichier. La signification de cette valeur dépend de l’indicateur spécifié dans **lChangeFlag**.

</dd> <dt>

<span id="lChangeFlag"></span><span id="lchangeflag"></span><span id="LCHANGEFLAG"></span>*lChangeFlag*
</dt> <dd>

Indicateur spécifiant le mode de modification de la position de fichier. Les valeurs suivantes sont définies :



| Condition requise | Valeur |
|-----------|------------------------------------------------------------------------------------------------------------------------|
| SEEK \_ cur | Déplacez la position de fichier en octets *lNewFilePos* à partir de la position actuelle. *lNewFilePos* peut être positif ou négatif. |
| fin de recherche \_ | Déplacez la position de fichier à *lNewFilePos* octets à partir de la fin du fichier.                                             |
| ensemble de recherches \_ | Déplacez la position de fichier à *lNewFilePos* octets à partir du début du fichier.                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la nouvelle position de fichier. En cas d’erreur, la valeur de retour est 1.

## <a name="remarks"></a>Notes

La procédure d’e/s est responsable de la gestion de la position de fichier actuelle dans le membre **lDiskOffset** de la structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>MMSYSTEM. h (inclure Windows. h)</dt> </dl> |



 

