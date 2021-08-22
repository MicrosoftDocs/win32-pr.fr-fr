---
title: Message EM_TAKEFOCUS (commctrl. h)
description: Force un contrôle d’édition sur une seule ligne à recevoir le focus clavier. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro modifier TakeFocus.
ms.assetid: 27470857-4219-4426-bc69-e1271afc6ffb
keywords:
- EM_TAKEFOCUS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_TAKEFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8283f2f9ea033439ef9ad7ec0ce40b08bb6396db8f5ebc7a9b1d513f29c209a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437139"
---
# <a name="em_takefocus-message"></a>\_Message TAKEFOCUS em

\[Destiné à un usage interne ; non recommandé pour une utilisation dans les applications. Ce message n’est peut-être pas pris en charge dans les versions ultérieures de Windows.\]

Force un contrôle d’édition sur une seule ligne à recevoir le focus clavier. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**modifier \_ TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour n’est pas utilisée.

## <a name="security-considerations"></a>Considérations relatives à la sécurité

L’utilisation de ce message peut compromettre la sécurité de votre programme.

## <a name="remarks"></a>Remarques

Ce message est ignoré si le contrôle d’édition n’est pas un contrôle d’édition sur une seule ligne.

Si le contrôle d’édition a précédemment reçu un message [**em \_ NOSETFOCUS**](em-nosetfocus.md) , le contrôle d’édition semble avoir le focus sans réellement l’avoir ; sinon, le contrôle d’édition reçoit le focus.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**Modifier \_ TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus)
</dt> <dt>

[**\_NOSETFOCUS em**](em-nosetfocus.md)
</dt> </dl>

 

 





