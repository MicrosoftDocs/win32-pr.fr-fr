---
title: Message UDM_GETPOS32 (commctrl. h)
description: Retourne la position 32 bits d’un contrôle up-up.
ms.assetid: 90feffbd-a472-446f-8a67-5da408cde002
keywords:
- UDM_GETPOS32 les contrôles de message Windows
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
ms.openlocfilehash: 15f316b6833c67cd01d4e01910399a8730691f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464647"
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

## <a name="remarks"></a>Notes

Lors du traitement de ce message, le contrôle up-out met à jour sa position actuelle en fonction de la légende de la fenêtre associée. Elle retourne une erreur s’il n’existe aucune fenêtre associée ou si la légende spécifie une valeur non valide ou hors limites.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
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

 

 





