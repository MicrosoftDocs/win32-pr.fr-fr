---
title: Message UDM_SETPOS (commctrl. h)
description: Définit la position actuelle d’un contrôle up-up avec une précision de 16 bits.
ms.assetid: e7c8b55f-3a4f-47e7-8c7d-e47509f27f1d
keywords:
- UDM_SETPOS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- UDM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b409f9e7468e3add89248b61b7b563ac592f0dcc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115433"
---
# <a name="udm_setpos-message"></a>\_Message SetPos UDM

Définit la position actuelle d’un contrôle up-up avec une précision de 16 bits.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Nouvelle position pour le contrôle up-up. Si le paramètre est en dehors de la plage spécifiée du contrôle, *lParam* prend la valeur valide la plus proche.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est la position précédente.

## <a name="remarks"></a>Notes

Ce message ne prend en charge que les positions 16 bits. Si les valeurs 32 bits ont été activées pour un contrôle up-out avec [**UDM \_ SETRANGE32**](udm-setrange32.md), utilisez [**UDM \_ SETPOS32**](udm-setpos32.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_GETRANGE UDM**](udm-getrange.md)
</dt> <dt>

[**\_GETPOS UDM**](udm-getpos.md)
</dt> </dl>

 

 





