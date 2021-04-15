---
title: Message EM_TAKEFOCUS (commctrl. h)
description: Force un contrôle d’édition sur une seule ligne à recevoir le focus clavier. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro modifier TakeFocus.
ms.assetid: 27470857-4219-4426-bc69-e1271afc6ffb
keywords:
- EM_TAKEFOCUS les contrôles de message Windows
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
ms.openlocfilehash: 5e4abdf926cdd337760b5cf151c3f8ee08cb418b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465382"
---
# <a name="em_takefocus-message"></a>\_Message TAKEFOCUS em

\[Destiné à un usage interne ; non recommandé pour une utilisation dans les applications. Ce message n’est peut-être pas pris en charge dans les versions futures de Windows.\]

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

## <a name="remarks"></a>Notes

Ce message est ignoré si le contrôle d’édition n’est pas un contrôle d’édition sur une seule ligne.

Si le contrôle d’édition a précédemment reçu un message [**em \_ NOSETFOCUS**](em-nosetfocus.md) , le contrôle d’édition semble avoir le focus sans réellement l’avoir ; sinon, le contrôle d’édition reçoit le focus.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**Modifier \_ TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus)
</dt> <dt>

[**\_NOSETFOCUS em**](em-nosetfocus.md)
</dt> </dl>

 

 





