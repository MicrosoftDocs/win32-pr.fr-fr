---
title: Message LVM_SETCALLBACKMASK (commctrl. h)
description: Modifie le masque de rappel pour un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetCallbackMask.
ms.assetid: d7828bab-9897-408c-99ca-fad42b431be8
keywords:
- LVM_SETCALLBACKMASK les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef6dd46228c4e4aeada30f469a77f9e67aff3a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103364"
---
# <a name="lvm_setcallbackmask-message"></a>\_Message SETCALLBACKMASK LVM

Modifie le masque de rappel pour un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur du masque de rappel. Les bits du masque indiquent les États ou images d’élément pour lesquels l’application stocke les données d’état actuelles. Cette valeur peut être n’importe quelle combinaison des constantes suivantes :



| Valeur                                                                                                                                                                           | Signification                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS \_ couper**</dt> </dl>                                  | L’élément est marqué pour une opération couper-coller.<br/>                                       |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS \_ DROPHILITED**</dt> </dl>          | L’élément est mis en surbrillance en tant que cible de glisser-déplacer.<br/>                                      |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS \_ concentré**</dt> </dl>                      | L’élément a le focus.<br/>                                                                 |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ sélectionné**</dt> </dl>                   | L'élément est sélectionné. <br/>                                                                  |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**LVIS \_ OVERLAYMASK**</dt> </dl>          | L’application stocke l’index de liste d’images de l’image de superposition actuelle pour chaque élément.<br/> |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS \_ STATEIMAGEMASK**</dt> </dl> | L’application stocke l’index de liste d’images de l’image d’État actuelle pour chaque élément. <br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Le *masque de rappel* d’un contrôle List-View est un jeu d’indicateurs binaires qui spécifient les États de l’élément pour lesquels l’application, plutôt que le contrôle, stocke les données actuelles. Le masque de rappel s’applique à tous les éléments du contrôle, contrairement à la désignation de l’élément de rappel, qui s’applique à un élément spécifique. Le masque de rappel a la valeur zéro par défaut, ce qui signifie que le contrôle List-View stocke toutes les informations sur l’état de l’élément. Après avoir créé un contrôle List-View et initialisé ses éléments, vous pouvez envoyer le **message \_ SETCALLBACKMASK LVM** pour modifier le masque de rappel. Pour récupérer le masque de rappel actuel, envoyez le message [**\_ GETCALLBACKMASK LVM**](lvm-getcallbackmask.md) .

Pour plus d’informations sur les images de superposition et les images d’État, consultez [Ajout de listes d’images List-View](using-list-view-controls.md).

Pour plus d’informations sur les rappels de vue de liste, consultez [éléments de rappel et masque de rappel](list-view-controls-overview.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LVN \_ GETDISPINFO**](lvn-getdispinfo.md)
</dt> </dl>

 

 





