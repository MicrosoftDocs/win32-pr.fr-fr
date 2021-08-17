---
title: Message LVM_GETITEMSTATE (commctrl. h)
description: Récupère l’état d’un élément de vue liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetItemState.
ms.assetid: 862960ed-a64a-4d66-b384-9228932eae6f
keywords:
- LVM_GETITEMSTATE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4737be14f3e975f87a6cbea460ef53dd40ecbb7b6a2d06c39a247dbe8aa0a14e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958298"
---
# <a name="lvm_getitemstate-message"></a>\_Message GETITEMSTATE LVM

Récupère l’état d’un élément de vue liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’élément de vue de liste.

</dd> <dt>

*lParam* 
</dt> <dd>

Informations d’État à récupérer. Ce paramètre peut être une combinaison des valeurs suivantes :



| Valeur                                                                                                                                                                           | Signification                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS \_ couper**</dt> </dl>                                  | L’élément est marqué pour une opération couper-coller.<br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS \_ DROPHILITED**</dt> </dl>          | L’élément est mis en surbrillance en tant que cible de glisser-déplacer.<br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS \_ concentré**</dt> </dl>                      | L’élément a le focus, donc il est entouré d’un rectangle de focus standard. Bien qu’un seul élément puisse être sélectionné, un seul élément peut avoir le focus.<br/> |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ sélectionné**</dt> </dl>                   | L'élément est sélectionné. L’apparence d’un élément sélectionné varie selon qu’il a le focus et également sur les couleurs système utilisées pour la sélection.<br/>             |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**LVIS \_ OVERLAYMASK**</dt> </dl>          | Utilisez ce masque pour récupérer l’index de l’image de superposition de l’élément.<br/>                                                                                                 |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS \_ STATEIMAGEMASK**</dt> </dl> | Utilisez ce masque pour récupérer l’index de l’image d’état de l’élément.<br/>                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’état actuel de l’élément spécifié. Les seuls bits valides dans la valeur de retour sont ceux qui correspondent aux bits définis dans le paramètre *lParam* .

## <a name="remarks"></a>Remarques

Les informations d’état d’un élément incluent un jeu d’indicateurs binaires, ainsi que des index de liste d’images qui indiquent l’image d’état de l’élément et l’image de superposition.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETITEMSTATE LVM**](lvm-setitemstate.md)
</dt> </dl>

 

 





