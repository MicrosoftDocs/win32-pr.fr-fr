---
title: Message TTM_TRACKPOSITION (commctrl. h)
description: Définit la position d’une info-bulle de suivi.
ms.assetid: 9eb7c86c-78e6-442a-ad77-5fb919cab591
keywords:
- TTM_TRACKPOSITION les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_TRACKPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6eab8184049d8bf876a7e782b9adc2091d5fac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033011"
---
# <a name="ttm_trackposition-message"></a>\_Message atténuation TRACKPOSITION

Définit la position d’une info-bulle de suivi.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la coordonnée x du point auquel l’info-bulle de suivi sera affichée, en coordonnées d’écran. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la coordonnée y du point auquel l’info-bulle de suivi sera affichée, en coordonnées d’écran.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de ce message n’est pas utilisée.

## <a name="remarks"></a>Notes

Le contrôle ToolTip choisit où afficher la fenêtre d’info-bulle en fonction des coordonnées que vous fournissez avec ce message. La fenêtre d’info-bulle s’affiche alors à côté de l’outil auquel elle correspond. Pour que les fenêtres d’info-bulle s’affichent à des coordonnées spécifiques, incluez l' \_ indicateur de l’Absolute dans le membre **uFlags** de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) lors de l’ajout de l’outil.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**ATTÉNUATION \_ TRACKACTIVATE**](ttm-trackactivate.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Utilisation des contrôles ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

