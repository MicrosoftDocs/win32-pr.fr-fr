---
title: Message IPM_GETADDRESS (commctrl. h)
description: Obtient les valeurs d’adresse pour les quatre champs dans le contrôle d’adresse IP.
ms.assetid: 4fe68d45-7d7f-46da-a110-65f899b3c393
keywords:
- IPM_GETADDRESS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- IPM_GETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 426e9c76712701b2f4e108679133be23eb700687
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999897"
---
# <a name="ipm_getaddress-message"></a>\_Message de message de message IPM

Obtient les valeurs d’adresse pour les quatre champs dans le contrôle d’adresse IP.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une valeur **DWORD** qui reçoit l’adresse. La valeur du champ 3 sera comprise entre bits 0 et 7. La valeur du champ 2 sera contenue dans les bits 8 à 15. La valeur du champ 1 est comprise entre les bits 16 et 23. La valeur du champ 0 sera contenue dans les bits de 24 à 31. Les [**premières \_**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)macros IPAddress, [**second \_**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress)IPAddress, [**troisième \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)et quatrième sont également utilisables pour extraire les informations d’adresse. [**\_**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) La valeur zéro est renvoyée en tant qu’adresse pour tous les champs vides.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne le nombre de champs non vides.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





