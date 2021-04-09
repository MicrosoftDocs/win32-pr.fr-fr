---
title: Message LVM_CREATEDRAGIMAGE (commctrl. h)
description: Crée une liste d’images de glissement pour l’élément spécifié. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView CreateDragImage.
ms.assetid: face4c8f-01ff-4f5a-a468-e306a50dae35
keywords:
- LVM_CREATEDRAGIMAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace975b178fee85e2794b518a78b40b375c65ae7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102905"
---
# <a name="lvm_createdragimage-message"></a>\_Message CREATEDRAGIMAGE LVM

Crée une liste d’images de glissement pour l’élément spécifié. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l'élément.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure de [**points**](/previous-versions//dd162805(v=vs.85)) qui reçoit l’emplacement initial de l’angle supérieur gauche de l’image, en coordonnées de vue.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle de la liste d’images de glissement en cas de réussite, ou **null** dans le cas contraire.

## <a name="remarks"></a>Notes

Votre application est responsable de la destruction de la liste d’images lorsqu’elle n’est plus nécessaire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

