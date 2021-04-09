---
title: Message RB_GETBANDINFO (commctrl. h)
description: Récupère des informations sur une bande spécifiée dans un contrôle rebar.
ms.assetid: c2a76c91-7d44-4278-823d-bd263520e7a8
keywords:
- RB_GETBANDINFO les contrôles de message Windows
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
ms.openlocfilehash: b87715cf61b4eb2726eab83d500330721f41719f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104791"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **RB \_ GETBANDINFOW** (Unicode) et **RB \_ GETBANDINFOA** (ANSI)<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETBANDINFO RB**](rb-setbandinfo.md)
</dt> </dl>

 

 





