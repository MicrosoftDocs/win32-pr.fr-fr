---
title: Message MMIOM_CLOSE (mmsystem. h)
description: Le \_ message MMIOM Close est envoyé à une procédure d’e/s par la fonction mmioClose pour demander la fermeture d’un fichier.
ms.assetid: 9d0dad5b-fd0a-4948-a4cf-9d138e353c76
keywords:
- Message MMIOM_CLOSE Windows Multimedia
topic_type:
- apiref
api_name:
- MMIOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7863698b99bcead8bc22e6194d213bbc663d5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519297"
---
# <a name="mmiom_close-message"></a>MMIOM \_ Fermer le message

Le message **MMIOM \_ Close** est envoyé à une procédure d’e/s par la fonction [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) pour demander la fermeture d’un fichier.


```C++
MMIOM_CLOSE 
lParam1 = (LPARAM) lCloseFlags 
lParam2 = reserved 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*lCloseFlags*
</dt> <dd>

Indicateurs contenus dans le paramètre **wFlags** de **mmioClose**.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro si le fichier est fermé avec succès ou une erreur dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>MMSYSTEM. h (inclure Windows. h)</dt> </dl> |



 

