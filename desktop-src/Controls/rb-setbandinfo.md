---
title: Message RB_SETBANDINFO (commctrl. h)
description: Définit les caractéristiques d’une bande existante dans un contrôle rebar.
ms.assetid: 00021c35-612d-4278-b10c-6e9f1f45a543
keywords:
- RB_SETBANDINFO les contrôles de Windows de message
topic_type:
- apiref
api_name:
- RB_SETBANDINFO
- RB_SETBANDINFOA
- RB_SETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e81377a40f8b6054f5d8cfae16837621b77b61
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117250"
---
# <a name="rb_setbandinfo-message"></a>\_Message SETBANDINFO RB

Définit les caractéristiques d’une bande existante dans un contrôle rebar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la bande devant recevoir les nouveaux paramètres.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) qui définit la bande à modifier et les nouveaux paramètres. Avant d’envoyer ce message, vous devez définir la structure **sizeof**(REBARBANDINFO) pour le membre **cbSize** de cette structure. En outre, vous devez définir le membre **CCH** de la structure **REBARBANDINFO** sur la taille de la mémoire tampon **lpText** lorsque le \_ texte RBBIM est spécifié.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **RB \_ SETBANDINFOW** (Unicode) et **RB \_ SETBANDINFOA** (ANSI)<br/>             |



 

 





