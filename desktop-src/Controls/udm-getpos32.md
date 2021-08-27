---
title: Message UDM_GETPOS32 (commctrl. h)
description: Retourne la position 32 bits d’un contrôle up-up.
ms.assetid: 90feffbd-a472-446f-8a67-5da408cde002
keywords:
- UDM_GETPOS32 les contrôles de Windows de message
topic_type:
- apiref
api_name:
- UDM_GETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11d043ca4f6b69a554b43d5abeaf35e4c2a2a6d72797e829900529df70b6c47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059789"
---
# <a name="udm_getpos32-message"></a>\_Message GETPOS32 UDM

Retourne la position 32 bits d’un contrôle up-up.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une valeur **bool** qui a la valeur zéro si la valeur est récupérée avec succès ou différente de zéro si une erreur se produit. Si ce paramètre a la valeur **null**, les erreurs ne sont pas signalées.

Si **UDM \_ GETPOS32** est utilisé dans une situation inter-processus, ce paramètre doit avoir la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la position d’un contrôle up-up avec une précision de 32 bits. Les applications doivent vérifier la valeur *lParam* pour déterminer si la valeur de retour est valide.

## <a name="remarks"></a>Remarques

Lors du traitement de ce message, le contrôle up-out met à jour sa position actuelle en fonction de la légende de la fenêtre associée. Elle retourne une erreur s’il n’existe aucune fenêtre associée ou si la légende spécifie une valeur non valide ou hors limites.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_GETPOS UDM**](udm-getpos.md)
</dt> <dt>

[**\_SetPos UDM**](udm-setpos.md)
</dt> <dt>

[**\_SETPOS32 UDM**](udm-setpos32.md)
</dt> </dl>

 

 





