---
title: HDN_DROPDOWN le code de notification (commctrl. h)
description: Envoyé par un contrôle d’en-tête à son parent lorsque l’utilisateur clique sur la flèche déroulante du contrôle d’en-tête. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: cacf5cb9-0593-42ff-868d-b098481f565f
keywords:
- HDN_DROPDOWN les contrôles de Windows de code de notification
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999938"
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

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

L’exemple de la section syntaxe montre comment le récepteur de notification convertit **lParam** pour récupérer la structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) . **WParam** contient l’ID du contrôle qui envoie ce message.

Ce message est envoyé uniquement si le style HDF \_ SPLITBUTTON est défini sur l’élément d’en-tête.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





