---
title: Message RB_GETBANDINFO (commctrl. h)
description: Récupère des informations sur une bande spécifiée dans un contrôle rebar.
ms.assetid: c2a76c91-7d44-4278-823d-bd263520e7a8
keywords:
- RB_GETBANDINFO les contrôles de Windows de message
topic_type:
- apiref
api_name:
- RB_GETBANDINFO
- RB_GETBANDINFOA
- RB_GETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b0ae509699c23ad24b9b97451178f4711ab52176a9c15aeef757bab85c861c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409440"
---
# <a name="rb_getbandinfo-message"></a>\_Message GETBANDINFO RB

Récupère des informations sur une bande spécifiée dans un contrôle rebar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la bande pour laquelle les informations sont récupérées.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) qui recevra les informations de la bande demandée. Avant d’envoyer ce message, vous devez définir le membre **cbSize** de cette structure sur la taille de la structure **REBARBANDINFO** et définir le membre **fmask** sur les éléments que vous souhaitez récupérer. En outre, vous devez définir le membre **CCH** de la structure **REBARBANDINFO** sur la taille de la mémoire tampon **lpText** lorsque le \_ texte RBBIM est spécifié.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **RB \_ GETBANDINFOW** (Unicode) et **RB \_ GETBANDINFOA** (ANSI)<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETBANDINFO RB**](rb-setbandinfo.md)
</dt> </dl>

 

 





