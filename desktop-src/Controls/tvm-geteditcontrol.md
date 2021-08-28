---
title: Message TVM_GETEDITCONTROL (commctrl. h)
description: Récupère le handle du contrôle d’édition utilisé pour modifier le texte d’un élément d’affichage d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetEditControl TreeView.
ms.assetid: c89e57e8-e113-47a1-85e6-bb68990f9c1a
keywords:
- TVM_GETEDITCONTROL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a591104085de793d8ea479656eb9100424ba5194a173fd93d10444c43e2cbfc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104429"
---
# <a name="tvm_geteditcontrol-message"></a>TVM \_ GETEDITCONTROL message

Récupère le handle du contrôle d’édition utilisé pour modifier le texte d’un élément d’affichage d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetEditControl TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle du contrôle d’édition en cas de réussite, ou **null** dans le cas contraire.

## <a name="remarks"></a>Remarques

Lorsque la modification d’étiquette commence, un contrôle d’édition est créé, mais n’est pas positionné ni affiché. Avant qu’il ne soit affiché, le contrôle Tree-View envoie sa fenêtre parente à un code de notification [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) .

Pour personnaliser la modification des étiquettes, implémentez un gestionnaire pour [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) et envoyez un message **TVM \_ GETEDITCONTROL** au contrôle Tree-View. Si une étiquette est en cours de modification, la valeur de retour est un handle pour le contrôle d’édition. Utilisez ce handle pour personnaliser le contrôle d’édition en envoyant les messages **em \_ xxx** habituels.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





