---
title: Message TCM_SETITEMSIZE (commctrl. h)
description: Définit la largeur et la hauteur des onglets dans un contrôle onglet à largeur fixe ou owner-drawn. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetItemSize.
ms.assetid: 3935d686-f8bc-41fb-b025-04120cf03f02
keywords:
- TCM_SETITEMSIZE les contrôles de message Windows
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
ms.openlocfilehash: e306af3f6462507a181de91104169c5ac7d6ce14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843049"
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

## <a name="remarks"></a>Notes

Si la largeur est définie sur une valeur inférieure à la largeur d’image définie par [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create), la largeur de l’onglet est définie sur la valeur la plus faible qui est supérieure à la largeur de l’image.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

