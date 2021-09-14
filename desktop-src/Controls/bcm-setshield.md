---
title: Message BCM_SETSHIELD (commctrl. h)
description: Définit l’état d’élévation requis pour un bouton ou un lien de commande spécifié pour afficher une icône avec élévation de privilèges. Envoyez ce message explicitement ou à l’aide de la \_ macro Button SetElevationRequiredState.
ms.assetid: 2ce2a006-7136-415b-824b-46b282b100f4
keywords:
- BCM_SETSHIELD les contrôles de Windows de message
topic_type:
- apiref
api_name:
- BCM_SETSHIELD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2149e2945f2876309459c287961b7b0a4a1f9acf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920391"
---
# <a name="bcm_setshield-message"></a>\_Message SETSHIELD BCM

Définit l’état d’élévation requis pour un bouton ou un lien de commande spécifié pour afficher une icône avec élévation de privilèges. Envoyez ce message explicitement ou à l’aide de la macro [**Button \_ SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Valeur **booléenne** qui est **true** pour dessiner une icône avec élévation de privilèges, ou **false** dans le cas contraire.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne 1 en cas de réussite, ou un code d’erreur dans le cas contraire.

## <a name="remarks"></a>Notes

Une application doit être manifestée pour utiliser comctl32.dll version 6 pour obtenir cette fonctionnalité.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





