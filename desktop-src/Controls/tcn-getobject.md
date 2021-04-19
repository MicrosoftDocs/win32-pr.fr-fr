---
title: TCN_GETOBJECT le code de notification (commctrl. h)
description: Envoyé par un contrôle onglet lorsqu’il a le \_ \_ style étendu TCS ex REGISTERDROP et qu’un objet est glissé sur un élément d’onglet dans le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 0beddabe-0e97-4fe7-bcf7-adaba0d72dfe
keywords:
- Contrôles Windows de code de notification TCN_GETOBJECT
topic_type:
- apiref
api_name:
- TCN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e442a122397db717b25e71b17487866227476ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510114"
---
# <a name="tcn_getobject-notification-code"></a>\_Code de notification TCN GETOBJECT

Envoyé par un contrôle onglet lorsqu’il a le style étendu [**TCS \_ ex \_ REGISTERDROP**](tab-control-extended-styles.md) et qu’un objet est glissé sur un élément d’onglet dans le contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TCN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) qui contient des informations sur l’élément d’onglet sur lequel l’objet est glissé et reçoit les données retournées par l’application en réponse à ce message.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

L’application traitant ce code de notification doit retourner zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





