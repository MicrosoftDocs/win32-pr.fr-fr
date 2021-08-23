---
title: Message IPM_SETADDRESS (commctrl. h)
description: Définit les valeurs d’adresse pour les quatre champs dans le contrôle d’adresse IP.
ms.assetid: 52e72437-3558-4789-844f-5ab5b0b7967c
keywords:
- IPM_SETADDRESS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- IPM_SETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54817d2206295432e9b477532268a000fc43047ae928ab02224d668912474519
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434489"
---
# <a name="ipm_setaddress-message"></a>\_Message SETADDRESS IPM

Définit les valeurs d’adresse pour les quatre champs dans le contrôle d’adresse IP.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Valeur **DWORD** qui contient la nouvelle adresse. La valeur du champ 3 est comprise entre bits 0 et 7. La valeur du champ 2 est comprise entre bits 8 et 15. La valeur du champ 1 est comprise entre les bits 16 et 23. La valeur du champ 0 est comprise entre bits 24 et 31. La macro [**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) peut également être utilisée pour créer les informations d’adresse.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour n’est pas utilisée.

## <a name="remarks"></a>Remarques

Ce message ne génère pas de notification [**IPN \_ FIELDCHANGED**](ipn-fieldchanged.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





