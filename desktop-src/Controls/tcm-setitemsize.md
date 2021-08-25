---
title: Message TCM_SETITEMSIZE (commctrl. h)
description: Définit la largeur et la hauteur des onglets dans un contrôle onglet à largeur fixe ou owner-drawn. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetItemSize.
ms.assetid: 3935d686-f8bc-41fb-b025-04120cf03f02
keywords:
- TCM_SETITEMSIZE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TCM_SETITEMSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8845aa54cd3cca413f31ee01f4a9583e24dc875a876d1aff691f574214f6f793
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876229"
---
# <a name="tcm_setitemsize-message"></a>\_Message SETITEMSIZE TCM

Définit la largeur et la hauteur des onglets dans un contrôle onglet à largeur fixe ou owner-drawn. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ SetItemSize**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est une valeur **int** qui spécifie la nouvelle largeur, en pixels. Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) est une valeur **int** qui spécifie la nouvelle hauteur, en pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’ancienne largeur et la hauteur. La largeur est dans le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) de la valeur de retour et la hauteur est dans le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).

## <a name="remarks"></a>Remarques

Si la largeur est définie sur une valeur inférieure à la largeur d’image définie par [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create), la largeur de l’onglet est définie sur la valeur la plus faible qui est supérieure à la largeur de l’image.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

