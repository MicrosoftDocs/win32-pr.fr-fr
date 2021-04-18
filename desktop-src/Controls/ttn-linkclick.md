---
title: TTN_LINKCLICK le code de notification (commctrl. h)
description: Envoyé lorsqu’un clic est effectué sur un lien de texte à l’intérieur d’une info-bulle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: d3e76431-5b5f-4d67-8528-db21fd939917
keywords:
- Contrôles Windows de code de notification TTN_LINKCLICK
topic_type:
- apiref
api_name:
- TTN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90be24910c2739b4495b651abf97156342d955b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512816"
---
# <a name="ttn_linkclick-notification-code"></a>\_Code de notification ttn LINKCLICK

Envoyé lorsqu’un clic est effectué sur un lien de texte à l’intérieur d’une info-bulle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TTN_LINKCLICK
```



## <a name="parameters"></a>Paramètres

Ce code de notification n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Valeur de retour non utilisée.

## <a name="remarks"></a>Notes

Voici un exemple de l’envoi de cette notification. Supposons que votre info-bulle contient le texte suivant : « Ceci est un <A>lien</A>». Quand l’utilisateur clique sur « Link », le contrôle ToolTip envoie un \_ Code de notification ttn LINKCLICK.

> [!Note]  
> Pour utiliser ce code de notification, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





