---
title: Message DTM_GETSYSTEMTIME (commctrl. h)
description: Obtient l’heure actuellement sélectionnée à partir d’un contrôle de sélecteur de dates et d’heures (PAO) et la place dans une structure SYSTEMTIME spécifiée. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro DateTime GetSystemtime.
ms.assetid: 81c95187-109c-4b36-98ea-a2e77ce42d9a
keywords:
- DTM_GETSYSTEMTIME les contrôles de message Windows
topic_type:
- apiref
api_name:
- DTM_GETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e14d8c998720cc987a03877e1918e97304bf769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104842"
---
# <a name="dtm_getsystemtime-message"></a>\_Message DTM GETSYSTEMTIME

Obtient l’heure actuellement sélectionnée à partir d’un contrôle de sélecteur de dates et d’heures (PAO) et la place dans une structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) spécifiée. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ GetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) . Si **DTM \_ GETSYSTEMTIME** retourne GDT \_ valide, cette structure contiendra l’heure actuellement sélectionnée. Dans le cas contraire, il ne contient pas d’informations valides. Ce paramètre doit être un pointeur valide ; elle ne peut pas être **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne GDT \_ valide si les informations d’heure ont été placées avec succès dans *lParam*. Retourne GDT \_ None si le contrôle a été défini sur le style [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) et que la case à cocher Control n’a pas été activée. Retourne \_ une erreur GDT si une erreur se produit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

