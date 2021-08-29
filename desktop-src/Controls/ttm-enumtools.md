---
title: Message TTM_ENUMTOOLS (commctrl. h)
description: Récupère les informations qu’un contrôle ToolTip gère à propos de l’outil actuel \ 8212 ; autrement dit, l’outil pour lequel l’info-bulle affiche actuellement du texte.
ms.assetid: c470db71-c24c-45f4-b497-e59811017eee
keywords:
- TTM_ENUMTOOLS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TTM_ENUMTOOLS
- TTM_ENUMTOOLSA
- TTM_ENUMTOOLSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7534169bb0808daa63e835d3a46bf4ab31c059b63267727d5c4dbf43f28864d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769479"
---
# <a name="ttm_enumtools-message"></a>\_Message atténuation ENUMTOOLS

Récupère les informations qu’un contrôle ToolTip gère à propos de l’outil actuel, c’est-à-dire l’outil pour lequel l’info-bulle affiche actuellement du texte.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de l’outil pour lequel des informations doivent être récupérées.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) qui reçoit des informations sur l’outil. Définissez le membre **cbSize** de cette structure sur sizeof (TOOLINFO) avant d’envoyer ce message. Allouez une mémoire tampon. Définissez le membre **lpszText** pour qu’il pointe vers la mémoire tampon pour recevoir le texte de l’outil. Il n’existe aucun moyen de déterminer la taille de mémoire tampon requise. Toutefois, le texte d’outil, tel qu’il est retourné au membre **lpszText** de la structure **TOOLINFO** , a une longueur maximale de 80 **TCHARs**, y compris le caractère **null** de fin. Si le texte dépasse cette longueur, il est tronqué.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur false** , qu’un outil ait ou non été énuméré.

## <a name="remarks"></a>Remarques

**Avertissement de sécurité :** L’utilisation de ce message peut compromettre la sécurité de votre programme. Ce message ne permet pas au destinataire du message de connaître la taille de la mémoire tampon ou de spécifier la taille de la mémoire tampon. vous devez examiner les [considérations relatives à la sécurité : contrôles Microsoft Windows](sec-comctls.md) avant de continuer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **Atténuation \_ ENUMTOOLSW** (Unicode) et **atténuation \_ ENUMTOOLSA** (ANSI)<br/>               |



 

 





