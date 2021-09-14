---
title: Message DTM_GETSYSTEMTIME (commctrl. h)
description: Obtient l’heure actuellement sélectionnée à partir d’un contrôle de sélecteur de dates et d’heures (PAO) et la place dans une structure SYSTEMTIME spécifiée. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro DateTime GetSystemtime.
ms.assetid: 81c95187-109c-4b36-98ea-a2e77ce42d9a
keywords:
- DTM_GETSYSTEMTIME les contrôles de Windows de message
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239357"
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

## <a name="return-value"></a>Valeur de retour

Retourne GDT \_ valide si les informations d’heure ont été placées avec succès dans *lParam*. Retourne GDT \_ None si le contrôle a été défini sur le style [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) et que la case à cocher Control n’a pas été activée. Retourne \_ une erreur GDT si une erreur se produit.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

