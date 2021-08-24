---
title: Message LB_GETHORIZONTALEXTENT (winuser. h)
description: Obtient la largeur, en pixels, qu’une zone de liste peut faire défiler horizontalement (la largeur avec défilement) si la zone de liste a une barre de défilement horizontale.
ms.assetid: 52461724-c06a-436a-ac95-94c5189ba37e
keywords:
- LB_GETHORIZONTALEXTENT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01f754b62ad0f51a236662fdfba2304221d58e1288e2756c0330343c63a0699e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799509"
---
# <a name="lb_gethorizontalextent-message"></a>\_Message GETHORIZONTALEXTENT lb

Obtient la largeur, en pixels, qu’une zone de liste peut faire défiler horizontalement (la largeur avec défilement) si la zone de liste a une barre de défilement horizontale.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est la largeur de défilement, en pixels, de la zone de liste.

## <a name="remarks"></a>Remarques

Pour répondre au message **lb \_ GETHORIZONTALEXTENT** , la zone de liste doit avoir été définie avec le style [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) .

Si l’application ne définit pas l’étendue horizontale de la zone de liste (à l’aide de [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)), l’étendue horizontale par défaut est zéro. Notez que la zone de liste ne met pas à jour son étendue horizontale de manière dynamique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETHORIZONTALEXTENT lb**](lb-sethorizontalextent.md)
</dt> </dl>

 

