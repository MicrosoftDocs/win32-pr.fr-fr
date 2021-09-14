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
ms.openlocfilehash: 506f6193ab32d059bb85fa4583441bfbe027f224
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012300"
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

## <a name="return-value"></a>Valeur de retour

**True** en cas de réussite ; sinon, **false**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





