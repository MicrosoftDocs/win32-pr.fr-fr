---
title: Message TVM_GETEDITCONTROL (commctrl. h)
description: Récupère le handle du contrôle d’édition utilisé pour modifier le texte d’un élément d’affichage d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetEditControl TreeView.
ms.assetid: c89e57e8-e113-47a1-85e6-bb68990f9c1a
keywords:
- TVM_GETEDITCONTROL les contrôles de message Windows
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
ms.openlocfilehash: 79b4ce0beb125218e65c2c342caf59b57473088e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105961"
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

## <a name="remarks"></a>Notes

Lorsque la modification d’étiquette commence, un contrôle d’édition est créé, mais n’est pas positionné ni affiché. Avant qu’il ne soit affiché, le contrôle Tree-View envoie sa fenêtre parente à un code de notification [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) .

Pour personnaliser la modification des étiquettes, implémentez un gestionnaire pour [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) et envoyez un message **TVM \_ GETEDITCONTROL** au contrôle Tree-View. Si une étiquette est en cours de modification, la valeur de retour est un handle pour le contrôle d’édition. Utilisez ce handle pour personnaliser le contrôle d’édition en envoyant les messages **em \_ xxx** habituels.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





