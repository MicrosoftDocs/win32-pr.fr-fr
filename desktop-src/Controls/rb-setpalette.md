---
title: Message RB_SETPALETTE (commctrl. h)
description: Définit la palette actuelle du contrôle rebar.
ms.assetid: 85f0726a-21fd-41b3-aa52-6a0a0c1947fa
keywords:
- RB_SETPALETTE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- RB_SETPALETTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7ee47985c05bcd8a857620e7fe501bddf53bdec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117229"
---
# <a name="rb_setpalette-message"></a>\_Message SETPALETTE RB

Définit la palette actuelle du contrôle rebar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

**HPALETTE** qui spécifie la nouvelle palette que le contrôle rebar utilisera.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne un **HPALETTE** qui spécifie la palette précédente du contrôle rebar.

## <a name="remarks"></a>Notes

Il incombe à l’application d’envoyer ce message de supprimer le **HPALETTE** transmis dans ce message (voir [**SupprimerObjet**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)). Le contrôle rebar ne supprime pas un **HPALETTE** défini avec ce message.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETPALETTE RB**](rb-getpalette.md)
</dt> </dl>

 

