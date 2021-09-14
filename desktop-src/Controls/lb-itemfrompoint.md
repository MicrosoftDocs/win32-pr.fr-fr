---
title: Message LB_ITEMFROMPOINT (winuser. h)
description: Obtient l’index de base zéro de l’élément le plus proche du point spécifié dans une zone de liste.
ms.assetid: 5739eccb-e708-4ddb-ac97-d3e6c6120842
keywords:
- LB_ITEMFROMPOINT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_ITEMFROMPOINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c4f06b9de8e6580c81c7faf7ddb8c287a148b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999859"
---
# <a name="lb_itemfrompoint-message"></a>\_Message ITEMFROMPOINT lb

Obtient l’index de base zéro de l’élément le plus proche du point spécifié dans une zone de liste.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la coordonnée x d’un point, par rapport à l’angle supérieur gauche de la zone cliente de la zone de liste.

Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la coordonnée y d’un point, par rapport à l’angle supérieur gauche de la zone cliente de la zone de liste.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour contient l’index de l’élément le plus proche dans le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)). [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) est égal à zéro si le point spécifié se trouve dans la zone cliente de la zone de liste, ou un point s’il est en dehors de la zone cliente.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

