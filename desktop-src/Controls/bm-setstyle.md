---
title: Message BM_SETSTYLE (winuser. h)
description: Définit le style d’un bouton. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro Button SetStyle.
ms.assetid: 6439e68f-87fc-4a4a-8025-facc3c0e03e2
keywords:
- BM_SETSTYLE les contrôles de Windows de message
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
ms.openlocfilehash: 17f635a70bf806c6c26f5b236ea939bc453d27bf0fe135f8e2586aeb59021b9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674417"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



 

