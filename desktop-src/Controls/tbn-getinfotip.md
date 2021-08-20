---
title: TBN_GETINFOTIP le code de notification (commctrl. h)
description: Récupère les informations de l’info-bulle d’un élément de barre d’outils. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 877de60c-f6e1-440a-81f0-d66ab443c985
keywords:
- TBN_GETINFOTIP les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TBN_GETINFOTIP
- TBN_GETINFOTIPA
- TBN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6adb47a940ce6795047a1aca8bb7cbdc0899a142c132ab8f6f39e6bb089f1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077903"
---
# <a name="tbn_getinfotip-notification-code"></a>\_Code de notification TBN GETINFOTIP

Récupère les informations de l’info-bulle d’un élément de barre d’outils. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_GETINFOTIP

    lptbgit = (LPNMTBGETINFOTIP) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) qui contient des informations sur les éléments et reçoit des informations sur l’info-bulle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée par le contrôle.

## <a name="remarks"></a>Remarques

La prise en charge de l’info-bulle dans la barre d’outils permet à la barre d’outils d’afficher des info-bulles pour les éléments dont la taille est de INFOTIPSIZE caractères. Si ce code de notification n’est pas traité, la barre d’outils utilise le texte de l’élément pour l’info-bulle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TBN \_ GETINFOTIPW** (Unicode) et **TBN \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





