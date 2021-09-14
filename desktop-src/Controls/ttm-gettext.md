---
title: Message TTM_GETTEXT (commctrl. h)
description: Récupère les informations qu’un contrôle ToolTip gère à propos d’un outil.
ms.assetid: f2afa706-4209-4761-a981-df3d5b938c88
keywords:
- TTM_GETTEXT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TTM_GETTEXT
- TTM_GETTEXTA
- TTM_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f774671d34f89306593d23481fa917190ae69aaa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115862"
---
# <a name="ttm_gettext-message"></a>\_Message atténuation GETTEXT

Récupère les informations qu’un contrôle ToolTip gère à propos d’un outil.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Le nombre de **TCHARs**, y compris le caractère **null** de fin, à copier dans la mémoire tampon vers laquelle pointe **lpszText**. </dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . Définissez le membre **cbSize** de cette structure sur `sizeof(TOOLINFO)` avant d’envoyer ce message. Définissez les membres **HWND** et **UID** pour identifier l’outil pour lequel des informations doivent être récupérées. Allouez une mémoire tampon de taille spécifiée par *wParam*. Définissez le membre **lpszText** pour qu’il pointe vers la mémoire tampon pour recevoir le texte de l’outil.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **Atténuation \_ GETTEXTW** (Unicode) et **atténuation \_ gettexta** (ANSI)<br/>                   |



 

 





