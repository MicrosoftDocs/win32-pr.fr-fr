---
title: Message CB_GETCUEBANNER (winuser. h)
description: Obtient le texte de bannière de signal affiché dans le contrôle d’édition d’une zone de liste déroulante. Envoyez ce message explicitement ou à l’aide de la \_ macro ComboBox GetCueBannerText.
ms.assetid: 38959228-9f07-4636-a1ea-681efe77b9ec
keywords:
- CB_GETCUEBANNER les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_GETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866f51df0083c4cd72c3f34bb3ce045e0f577a24
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123897"
---
# <a name="cb_getcuebanner-message"></a>\_Message GETCUEBANNER CB

Obtient le texte de bannière de signal affiché dans le contrôle d’édition d’une zone de liste déroulante. Envoyez ce message explicitement ou à l’aide de la macro [**ComboBox \_ GetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon de chaîne Unicode qui reçoit le texte de bannière de signal. L’application appelante est chargée d’allouer la mémoire pour la mémoire tampon. La taille de la mémoire tampon doit être égale à la longueur de la chaîne de bannière de signal dans **WCHARs**, plus 1 pour le paramètre de fin **null** **WCHAR**.

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon vers laquelle pointe *lpcwText* dans **WCHARs**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne 1 en cas de réussite, ou une valeur d’erreur dans le cas contraire.

S’il n’y a aucun texte de bannière de signal à obtenir, la valeur de retour est 0. Si l’application appelante ne parvient pas à allouer une mémoire tampon, ou à définir *lParam* avant d’envoyer ce message, un comportement non défini peut se produire et la valeur de retour peut ne pas être fiable.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctionnalités de zone de liste modifiable](combo-box-features.md)
</dt> </dl>

 

 





