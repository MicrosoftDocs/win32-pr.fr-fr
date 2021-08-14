---
title: Message LVM_CREATEDRAGIMAGE (commctrl. h)
description: Crée une liste d’images de glissement pour l’élément spécifié. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView CreateDragImage.
ms.assetid: face4c8f-01ff-4f5a-a468-e306a50dae35
keywords:
- LVM_CREATEDRAGIMAGE les contrôles de Windows de message
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
ms.openlocfilehash: d551dfa7b14ecff8c9fd1efe015e173403c1b5981f294a18b3180a42cc03de63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411994"
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

## <a name="remarks"></a>Remarques

Votre application est responsable de la destruction de la liste d’images lorsqu’elle n’est plus nécessaire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

