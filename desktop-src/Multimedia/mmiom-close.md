---
title: Message MMIOM_CLOSE (mmsystem. h)
description: Le \_ message MMIOM Close est envoyé à une procédure d’e/s par la fonction mmioClose pour demander la fermeture d’un fichier.
ms.assetid: 9d0dad5b-fd0a-4948-a4cf-9d138e353c76
keywords:
- message MMIOM_CLOSE Windows Multimedia
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
ms.openlocfilehash: 17a26b8b2ffa80c7c522fa5cdcbfc5da3334e0d2b5e258e090932147bf85438c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065389"
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
| En-tête<br/>                   | <dl> <dt>Mmsystem. h (inclure Windows. h)</dt> </dl> |



 

