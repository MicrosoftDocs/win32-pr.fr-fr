---
title: Message TDM_SET_PROGRESS_BAR_RANGE (commctrl. h)
description: Définit les valeurs minimale et maximale de la barre de progression dans une boîte de dialogue de tâche.
ms.assetid: ca8b48bc-cf56-4678-bb3d-7c730a96d98c
keywords:
- TDM_SET_PROGRESS_BAR_RANGE les contrôles de Windows de message
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116062"
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

## <a name="return-value"></a>Valeur de retour

Retourne les valeurs minimale et maximale précédentes, en cas de réussite, ou zéro dans le cas contraire. [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient la valeur minimale et [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contient la valeur maximale.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

