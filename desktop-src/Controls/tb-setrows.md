---
title: Message TB_SETROWS (commctrl. h)
description: Définit le nombre de lignes de boutons dans une barre d’outils.
ms.assetid: d8ea7b80-d23e-4593-8eb1-d23808173fc9
keywords:
- TB_SETROWS les contrôles de message Windows
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
ms.openlocfilehash: 5d0065a3f5f6a277713e368177886ebd064ea132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033264"
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

## <a name="remarks"></a>Notes

Étant donné que le système ne scinde pas les groupes de boutons lors de la définition du nombre de lignes, le nombre de lignes résultant peut différer du nombre demandé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

