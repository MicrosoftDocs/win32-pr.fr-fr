---
title: Message LVM_GETEDITCONTROL (commctrl. h)
description: Obtient le handle du contrôle d’édition utilisé pour modifier le texte d’un élément d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetEditControl.
ms.assetid: 70450b24-9879-4be8-9bc9-f87008b66415
keywords:
- LVM_GETEDITCONTROL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29f7e7ac31b3d429ab32ac6564a47f859f0e5dc2207d991cb580173838a4c366
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968309"
---
# <a name="lvm_geteditcontrol-message"></a>\_Message GETEDITCONTROL LVM

Obtient le handle du contrôle d’édition utilisé pour modifier le texte d’un élément d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne le handle du contrôle d’édition en cas de réussite, ou **null** dans le cas contraire.

## <a name="remarks"></a>Remarques

Lorsque la modification d’étiquette commence, un contrôle d’édition est créé, positionné et initialisé. Avant qu’il ne soit affiché, le contrôle List-View envoie sa fenêtre parente à un code de notification [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) .

Pour personnaliser la modification des étiquettes, implémentez un gestionnaire pour [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) et envoyez-lui un message **\_ GETEDITCONTROL LVM** vers le contrôle List-View. Si une étiquette est en cours de modification, la valeur de retour est un handle pour le contrôle d’édition. Utilisez ce handle pour personnaliser le contrôle d’édition en envoyant les messages **em \_ xxx** habituels.

Lorsque l’utilisateur termine ou annule la modification, le contrôle d’édition est détruit et le descripteur n’est plus valide. Vous pouvez sous-définir le contrôle d’édition, mais vous ne devez pas le détruire. Pour annuler la modification, envoyez le contrôle d’affichage de liste à un message [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) .

L’élément de vue de liste en cours de modification est l’élément ayant actuellement le focus, c’est-à-dire l’élément dans l’État focus. Pour rechercher un élément en fonction de son état, utilisez le message [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GetEditControl ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol)
</dt> </dl>

 

