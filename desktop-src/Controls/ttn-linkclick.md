---
title: TTN_LINKCLICK le code de notification (commctrl. h)
description: Envoyé lorsqu’un clic est effectué sur un lien de texte à l’intérieur d’une info-bulle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: d3e76431-5b5f-4d67-8528-db21fd939917
keywords:
- TTN_LINKCLICK les contrôles de Windows de code de notification
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115761"
---
# <a name="ttn_linkclick-notification-code"></a>\_Code de notification ttn LINKCLICK

Envoyé lorsqu’un clic est effectué sur un lien de texte à l’intérieur d’une info-bulle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TTN_LINKCLICK
```



## <a name="parameters"></a>Paramètres

Ce code de notification n’a pas de paramètres.

## <a name="return-value"></a>Valeur de retour

Valeur de retour non utilisée.

## <a name="remarks"></a>Notes

Voici un exemple de l’envoi de cette notification. Supposons que votre info-bulle contient le texte suivant : « Ceci est un <A>lien</A>». Quand l’utilisateur clique sur « Link », le contrôle ToolTip envoie un \_ Code de notification ttn LINKCLICK.

> [!Note]  
> Pour utiliser ce code de notification, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





