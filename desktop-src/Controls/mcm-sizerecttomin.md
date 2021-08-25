---
title: Message MCM_SIZERECTTOMIN (commctrl. h)
description: Calcule le nombre de calendriers qui tiennent dans le rectangle donné, puis retourne la taille minimale nécessaire pour qu’un rectangle tienne dans ce nombre de calendriers. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal SizeRectToMin.
ms.assetid: d52a7f68-e0c9-4646-a4aa-97129dffeb5d
keywords:
- MCM_SIZERECTTOMIN les contrôles de Windows de message
topic_type:
- apiref
api_name:
- MCM_SIZERECTTOMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547b8e401f270cbca1ff666ba0f1eb263ab3f9245f8a51e6874a7627597b9bfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799229"
---
# <a name="mcm_sizerecttomin-message"></a>\_Message SIZERECTTOMIN MCM

Calcule le nombre de calendriers qui tiennent dans le rectangle donné, puis retourne la taille minimale nécessaire pour qu’un rectangle tienne dans ce nombre de calendriers. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ SizeRectToMin**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Sur entrée, contient un pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui décrit une région qui est supérieure ou égale à la taille nécessaire pour s’adapter au nombre souhaité de calendriers. Lorsque cette fonction est retournée, contient la structure **Rect** minimale qui correspond à ce nombre de calendriers.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Inutilisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

