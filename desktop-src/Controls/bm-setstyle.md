---
title: Message BM_SETSTYLE (winuser. h)
description: Définit le style d’un bouton. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro Button SetStyle.
ms.assetid: 6439e68f-87fc-4a4a-8025-facc3c0e03e2
keywords:
- BM_SETSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- BM_SETSTYLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c080e1098d70b17e1e68bbbcd2d5598db79ef8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941851"
---
# <a name="bm_setstyle-message"></a>\_Message BM SETSTYLE

Définit le style d’un bouton. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**Button \_ SetStyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Style du bouton. Ce paramètre peut être une combinaison de styles de bouton. Pour obtenir un tableau de styles de bouton, consultez [styles de bouton](button-styles.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) de *lParam* est un **booléen** qui spécifie si le bouton doit être redessiné. La valeur **true** redessine le bouton. la valeur **false** ne redessine pas le bouton.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message retourne toujours la valeur zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



 

