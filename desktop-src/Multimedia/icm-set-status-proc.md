---
title: Message ICM_SET_STATUS_PROC (VFW. h)
description: le ICM \_ définir \_ le \_ message de procédure d’état fournit une fonction de rappel d’état avec l’état d’une opération de longue durée.
ms.assetid: a1bcd840-b94b-487e-91d6-67411a8a3a2d
keywords:
- message ICM_SET_STATUS_PROC Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_SET_STATUS_PROC
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02019bb6375aa18fd37ba34d2603839b37291d58822858b0b9cabc01e47d7b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678339"
---
# <a name="icm_set_status_proc-message"></a>ICM \_ DÉFINIR \_ le \_ message de procédure d’État

le **ICM définir le message de \_ \_ \_ procédure d’état** fournit une fonction de rappel d’état avec l’état d’une opération de longue durée.


```C++
ICM_SET_STATUS_PROC 
wParam = (DWORD_PTR)icsetstatusProc; 
lParam = sizeof(ICSETSTATUSPROC); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*icsetstatusProc*
</dt> <dd>

Pointeur vers une structure [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc) .

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Taille, en octets, de **ICSETSTATUSPROC**.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.

## <a name="remarks"></a>Remarques

La prise en charge de ce message est facultative, mais fortement recommandée si la compression ou la décompression prend plus d’un dixième de seconde environ.

Une application peut envoyer ce message périodiquement à une fonction de rappel d’État pendant des opérations de longue durée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestionnaire de compression vidéo](video-compression-manager.md)
</dt> <dt>

[Messages de compression vidéo](video-compression-messages.md)
</dt> </dl>

 

 





