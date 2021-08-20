---
title: Message MCM_GETCALENDARGRIDINFO (commctrl. h)
description: Obtient des informations sur une grille de calendrier.
ms.assetid: 6b385362-f963-4041-bc9f-d2b7a890c9b4
keywords:
- MCM_GETCALENDARGRIDINFO les contrôles de Windows de message
topic_type:
- apiref
api_name:
- MCM_GETCALENDARGRIDINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26365b940b17617b1f00b93697fc78fa759dd2599d3398ccb8d92725159a70cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170166"
---
# <a name="mcm_getcalendargridinfo-message"></a>\_Message GETCALENDARGRIDINFO MCM

Obtient des informations sur une grille de calendrier.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**MCGRIDINFO**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo) qui contient des informations sur la grille du calendrier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**True** en cas de réussite ; sinon, **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





