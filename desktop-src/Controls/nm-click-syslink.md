---
title: Code de notification NM_CLICK (Syslink) (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle que l’utilisateur a cliqué sur un lien hypertexte avec le bouton gauche de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: e92d7c92-f2c6-44aa-bce5-3bb07c184e7d
keywords:
- Windows les contrôles de code de notification d’NM_CLICK (syslink)
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8b3dd9b8ae4e0621898ceb50165af1d680340e352d6579a66e1f9355ec62e6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061749"
---
# <a name="nm_click-syslink-notification-code"></a>\_Code de notification de clic (Syslink) nm

Avertit la fenêtre parente d’un contrôle que l’utilisateur a cliqué sur un lien hypertexte avec le bouton gauche de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_CLICK

    pnmLink = (PNMLINK) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink) qui contient des informations supplémentaires sur cette notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée par le contrôle.

## <a name="remarks"></a>Remarques

> [!Note]  
> Pour utiliser ce code de notification, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink)
</dt> <dt>

[**\_notification WM**](wm-notify.md)
</dt> </dl>

 

 





