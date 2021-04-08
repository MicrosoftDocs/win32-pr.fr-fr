---
title: Message TDM_SET_PROGRESS_BAR_RANGE (commctrl. h)
description: Définit les valeurs minimale et maximale de la barre de progression dans une boîte de dialogue de tâche.
ms.assetid: ca8b48bc-cf56-4678-bb3d-7c730a96d98c
keywords:
- TDM_SET_PROGRESS_BAR_RANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_RANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17ebb6caa2c33282dccbb117980fc970cd45477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844365"
---
# <a name="tdm_set_progress_bar_range-message"></a>Message de plage de la barre de progression de l' \_ ensemble TDM \_ \_ \_

Définit les valeurs minimale et maximale de la barre de progression dans une boîte de dialogue de tâche.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la valeur minimale. Par défaut, la valeur minimale est zéro. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la valeur maximale. Par défaut, la valeur maximale est 100.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne les valeurs minimale et maximale précédentes, en cas de réussite, ou zéro dans le cas contraire. [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient la valeur minimale et [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contient la valeur maximale.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

