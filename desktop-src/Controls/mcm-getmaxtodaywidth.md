---
title: Message MCM_GETMAXTODAYWIDTH (commctrl. h)
description: Récupère la largeur maximale de \ 0034 ; Today \ 0034 ; chaîne dans un contrôle Month Calendar. Cela comprend le texte de l’étiquette et le texte de la date. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetMaxTodayWidth.
ms.assetid: bb55c24e-ba04-4a57-97b0-ff04d77e1d43
keywords:
- MCM_GETMAXTODAYWIDTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETMAXTODAYWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2b4c188e994a1dcc5a8fbd80ae3f1b06894bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741820"
---
# <a name="mcm_getmaxtodaywidth-message"></a>\_Message GETMAXTODAYWIDTH MCM

Récupère la largeur maximale de la chaîne « Today » dans un contrôle Month Calendar. Cela comprend le texte de l’étiquette et le texte de la date. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetMaxTodayWidth**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxtodaywidth) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la largeur de la chaîne « Today », en pixels.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





