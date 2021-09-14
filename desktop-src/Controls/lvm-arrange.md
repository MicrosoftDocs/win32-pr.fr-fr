---
title: Message LVM_ARRANGE (commctrl. h)
description: Organise les éléments en mode icône. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro organiser ListView.
ms.assetid: f7dbcdd2-3cc9-4bae-827e-8bac3b49486c
keywords:
- LVM_ARRANGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_ARRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a1b6a081cf963a649329951358ea4c972f200f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126924100"
---
# <a name="lvm_arrange-message"></a>\_Message d’organisation LVM

Organise les éléments en mode icône. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ organiser ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

L’une des valeurs suivantes qui spécifient l’alignement :



| Valeur                                                                                                                                                            | Signification                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span id="LVA_ALIGNLEFT"></span><span id="lva_alignleft"></span><dl> <dt>**LVA \_ ALIGNLEFT**</dt> </dl>    | Non implémenté. Appliquez le [**style \_ ALIGNLEFT LVS**](list-view-window-styles.md) à la place.<br/> |
| <span id="LVA_ALIGNTOP"></span><span id="lva_aligntop"></span><dl> <dt>**LVA \_ ALIGNTOP**</dt> </dl>       | Non implémenté. Appliquez le style [**LVS \_ ALIGNTOP**](list-view-window-styles.md) à la place.<br/>   |
| <span id="LVA_DEFAULT"></span><span id="lva_default"></span><dl> <dt>**LVA \_ par défaut**</dt> </dl>          | Aligne les éléments selon les styles d’alignement actuels du contrôle List-View (valeur par défaut).<br/>           |
| <span id="LVA_SNAPTOGRID"></span><span id="lva_snaptogrid"></span><dl> <dt>**LVA \_ SNAPTOGRID**</dt> </dl> | Aligne toutes les icônes à la position de grille la plus proche.<br/>                                                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite ; Sinon, **false**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





