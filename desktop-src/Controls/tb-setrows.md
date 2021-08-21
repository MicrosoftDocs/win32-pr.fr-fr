---
title: Message TB_SETROWS (commctrl. h)
description: Définit le nombre de lignes de boutons dans une barre d’outils.
ms.assetid: d8ea7b80-d23e-4593-8eb1-d23808173fc9
keywords:
- TB_SETROWS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_SETROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2c0e95d6f0f19c2b1c9b76cf22a37da0086987b22fe144603cdb2afa8a1ad83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293639"
---
# <a name="tb_setrows-message"></a>TO \_ SETROWS message

Définit le nombre de lignes de boutons dans une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie le nombre de lignes demandées. Le nombre minimal de lignes est un, et le nombre maximal de lignes est égal au nombre de boutons dans la barre d’outils.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) est un **booléen** qui indique s’il faut créer plus de lignes que ce qui est demandé lorsque le système ne peut pas créer le nombre de lignes spécifié par *wParam*. Si la **valeur est true**, le système crée plus de lignes. Si la **valeur est false**, le système crée moins de lignes.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui reçoit le rectangle englobant de la barre d’outils une fois les lignes définies.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Étant donné que le système ne scinde pas les groupes de boutons lors de la définition du nombre de lignes, le nombre de lignes résultant peut différer du nombre demandé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

