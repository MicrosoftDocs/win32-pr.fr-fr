---
title: Message IPM_SETADDRESS (commctrl. h)
description: Définit les valeurs d’adresse pour les quatre champs dans le contrôle d’adresse IP.
ms.assetid: 52e72437-3558-4789-844f-5ab5b0b7967c
keywords:
- IPM_SETADDRESS les contrôles de message Windows
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
ms.openlocfilehash: a8e8e4fa69791f93094d24f990ad62207cad33dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104464"
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

## <a name="remarks"></a>Notes

Ce message ne génère pas de notification [**IPN \_ FIELDCHANGED**](ipn-fieldchanged.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





