---
title: Message LVM_APPROXIMATEVIEWRECT (commctrl. h)
description: Calcule la largeur et la hauteur approximatives requises pour afficher un nombre donné d’éléments. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView ApproximateViewRect.
ms.assetid: a14331a8-217d-48c6-9489-fb90c4d31b91
keywords:
- LVM_APPROXIMATEVIEWRECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_APPROXIMATEVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97fcbb5476f28debd28116a52123bd01b8030c8b0a0c9c52e6598c864caed021
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047059"
---
# <a name="lvm_approximateviewrect-message"></a>\_Message APPROXIMATEVIEWRECT LVM

Calcule la largeur et la hauteur approximatives requises pour afficher un nombre donné d’éléments. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ ApproximateViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nombre d’éléments à afficher dans le contrôle. Si ce paramètre a la valeur-1, le message utilise le nombre total d’éléments dans le contrôle.

</dd> <dt>

*lParam* 
</dt> <dd>

Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est la dimension x proposée du contrôle, en pixels. Ce paramètre peut être défini sur-1 pour permettre au message d’utiliser la valeur de largeur actuelle.

Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) est la dimension y proposée du contrôle, en pixels. Ce paramètre peut être défini sur-1 pour permettre au message d’utiliser la valeur de la hauteur actuelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **DWORD** qui contient la largeur approximative (dans le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))) et la hauteur (dans le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))) nécessaire pour afficher les éléments, en pixels.

## <a name="remarks"></a>Remarques

La définition de la taille du contrôle d’affichage de liste en fonction des dimensions fournies par ce message peut optimiser le scintillement et réduire le scintillement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

