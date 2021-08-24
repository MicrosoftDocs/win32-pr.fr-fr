---
title: Message HDM_SETHOTDIVIDER (commctrl. h)
description: Modifie la couleur d’un séparateur entre des éléments d’en-tête pour indiquer la destination d’une opération de glisser-déplacer externe. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ SetHotDivider.
ms.assetid: 56f6e5c6-1df3-4b4d-9ad8-97fb168c5462
keywords:
- HDM_SETHOTDIVIDER les contrôles de Windows de message
topic_type:
- apiref
api_name:
- HDM_SETHOTDIVIDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eedfca7a6f0d10651984efb63c4db63116c4a53d2b9f9b85905c93fc12e6ca16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544749"
---
# <a name="hdm_sethotdivider-message"></a>\_Message HDM SETHOTDIVIDER

Modifie la couleur d’un séparateur entre des éléments d’en-tête pour indiquer la destination d’une opération de glisser-déplacer externe. Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ SetHotDivider**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Type de valeur représenté par *lParam*. Cette valeur peut être l'une des suivantes :



| Valeur                                                                                                                                    | Signification                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>VRAI * * * * *</dt> </dl>    | Indique que *lParam* contient les coordonnées clientes du pointeur.<br/> |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSe * * * * *</dt> </dl> | Indique que *lParam* contient une valeur d’index de séparateur.<br/>                 |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Une valeur contenue dans *lParam* est interprétée en fonction de la valeur de *wParam*.

Si *wParam* a la **valeur true**, *lParam* représente les coordonnées x et y du pointeur. La coordonnée x se trouve dans le mot de poids faible et la coordonnée y est dans le mot haut. Lorsque le contrôle header reçoit le message, il met en surbrillance le séparateur approprié en fonction des coordonnées *lParam* .

Si *wParam* a la **valeur false**, *lParam* représente l’index entier du séparateur à mettre en surbrillance.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur égale à l’index du séparateur mis en surbrillance par le contrôle.

## <a name="remarks"></a>Remarques

Ce message crée un effet qu’un contrôle header génère automatiquement lorsqu’il a le style [**HDS \_ DRAGDROP**](header-control-styles.md) . Le message **HDM \_ SETHOTDIVIDER** est destiné à être utilisé lorsque le propriétaire du contrôle gère manuellement les opérations de glisser-déplacer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





