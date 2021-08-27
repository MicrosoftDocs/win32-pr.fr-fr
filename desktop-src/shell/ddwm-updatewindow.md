---
description: Indique à une fenêtre d’image de dépôt d’effectuer la mise à jour à l’aide des nouvelles informations DROPDESCRIPTION.
title: Message DDWM_UPDATEWINDOW
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3b74f2e1-8121-4b7c-8d7a-b449cda529da
api_name:
- DDWM_UPDATEWINDOW
api_type:
- NA
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a17e015d6dff2ae5133f3ce8245c5ead3c3381f8eb5c48e74946fdf9bcb46ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032837"
---
# <a name="ddwm_updatewindow-message"></a>\_Message DDWM UPDATEWINDOW

Indique à une fenêtre d’image de dépôt d’effectuer la mise à jour à l’aide des nouvelles informations [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Non utilisé.

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="remarks"></a>Remarques

DDWM \_ UPDATEWINDOW est défini en tant qu' \_ utilisateur WM + 3.

Lorsque l’état d’une opération de suppression change (par exemple, en réponse à une touche de modification)[**IDropTarget ::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) retourne une nouvelle valeur [**DROPEFFECT**](../com/dropeffect-constants.md) (cette valeur **DROPEFFECT** peut également être reçue via [**IDropSource :: GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback)). En réponse, l’application met à jour la structure [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) de la cible de déplacement avec une nouvelle valeur [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) qui indique la décoration à appliquer au visuel de la fenêtre de glissement. par exemple, une indication que le fichier est copié plutôt que déplacé ou que l’objet ne peut pas être supprimé à cet emplacement. Toutefois, les éléments visuels ne sont pas mis à jour tant que l’objet n’a pas reçu un message **DDWM \_ UPDATEWINDOW** .

Le format de presse-papiers [DragWindow](clipboard.md) fournit le **HWND** de la fenêtre de glissement du destinataire à l’expéditeur du message **DDWM \_ UPDATEWINDOW** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 
