---
title: HDN_DROPDOWN le code de notification (commctrl. h)
description: Envoyé par un contrôle d’en-tête à son parent lorsque l’utilisateur clique sur la flèche déroulante du contrôle d’en-tête. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: cacf5cb9-0593-42ff-868d-b098481f565f
keywords:
- Contrôles Windows de code de notification HDN_DROPDOWN
topic_type:
- apiref
api_name:
- HDN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0ae7f2e2ee31feab1d8a2293913ac875a03718
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844489"
---
# <a name="hdn_dropdown-notification-code"></a>\_Code de notification de liste déroulante HDN

Envoyé par un contrôle d’en-tête à son parent lorsque l’utilisateur clique sur la flèche déroulante du contrôle d’en-tête. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_DROPDOWN
        
    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations sur le contrôle header.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

L’exemple de la section syntaxe montre comment le récepteur de notification convertit **lParam** pour récupérer la structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) . **WParam** contient l’ID du contrôle qui envoie ce message.

Ce message est envoyé uniquement si le style HDF \_ SPLITBUTTON est défini sur l’élément d’en-tête.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





