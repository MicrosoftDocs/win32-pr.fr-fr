---
description: Envoyé à la fonction CPlApplet d’une application du panneau de configuration pour récupérer le nombre de boîtes de dialogue prises en charge par l’application.
title: Message CPL_GETCOUNT (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6b88b56c-aad7-4144-ab95-15d7eef21861
api_name:
- CPL_GETCOUNT
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3bf8980fa29841d3c5341daeeccf26cea05db80c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412579"
---
# <a name="cpl_getcount-message"></a>\_Message Cpl GETCOUNT

Envoyé à la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) d’une application du panneau de configuration pour récupérer le nombre de boîtes de dialogue prises en charge par l’application.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) retourne le nombre de boîtes de dialogue que l’application du panneau de configuration prend en charge.

## <a name="remarks"></a>Notes

Ce message est envoyé immédiatement après le message d' [**\_ initialisation de cpl**](cpl-init.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>Cpl. h</dt> </dl> |



 

 
