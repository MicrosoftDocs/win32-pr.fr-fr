---
title: Message HDM_CREATEDRAGIMAGE (commctrl. h)
description: Crée une version semi-transparente de l’image d’un élément à utiliser comme image de glissement. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ CreateDragImage.
ms.assetid: 1b9dc515-d327-4634-a424-cc15a32f0f7c
keywords:
- HDM_CREATEDRAGIMAGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- HDM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1507f3e72ce75394aaad834fe5c0d876fc579a671ad8f2df00865b2278ad6e32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047229"
---
# <a name="hdm_createdragimage-message"></a>\_Message HDM CREATEDRAGIMAGE

Crée une version semi-transparente de l’image d’un élément à utiliser comme image de glissement. Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de l’élément dans le contrôle header. L’image assignée à cet élément est la base de l’image transparente.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un handle vers une liste d’images qui contient la nouvelle image comme son seul élément.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





