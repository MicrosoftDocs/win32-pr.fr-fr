---
title: Message TTM_HITTEST (commctrl. h)
description: Teste un point pour déterminer s’il se trouve dans le rectangle englobant de l’outil spécifié et, si c’est le cas, récupère des informations sur l’outil.
ms.assetid: d4dcc29b-c64c-41b8-a153-300df68ecdf5
keywords:
- TTM_HITTEST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TTM_HITTEST
- TTM_HITTESTA
- TTM_HITTESTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b515ccb5c283b66760f24c02749368e424e6fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115837"
---
# <a name="ttm_hittest-message"></a>\_Message atténuation HITTEST

Teste un point pour déterminer s’il se trouve dans le rectangle englobant de l’outil spécifié et, si c’est le cas, récupère des informations sur l’outil.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) . Lors de l’envoi du message, le membre **HWND** doit spécifier le descripteur d’un outil et le membre **PT** doit spécifier les coordonnées d’un point. Si la valeur de retour est **true**, le membre **TI** (une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) ) reçoit des informations sur l’outil qui occupe le point. Le membre **cbSize** de la structure **TI** doit être rempli avant l’envoi de ce message.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** si l’outil occupe le point spécifié, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Ce message doit être envoyé lorsque l’indicateur de piste TTF est défini pour l’outil \_ . Pour plus d’informations sur cet indicateur, consultez [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa). ATTÉNUATION \_ HITTEST échoue si \_ la piste ttf n’est pas définie, même si le point d’accès se trouve dans le rectangle d’outils.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **Atténuation \_ HITTESTW** (Unicode) et **atténuation \_ HITTESTA** (ANSI)<br/>                   |



 

 





