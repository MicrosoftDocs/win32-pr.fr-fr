---
title: Message UDM_GETPOS (commctrl. h)
description: Récupère la position actuelle d’un contrôle up-up avec une précision de 16 bits.
ms.assetid: 5f395de0-11b3-44f8-9bf4-42e27ce88a0c
keywords:
- UDM_GETPOS les contrôles de message Windows
topic_type:
- apiref
api_name:
- UDM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e78ad19289d85b93ebcb39a244a896ddb4f33f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510739"
---
# <a name="udm_getpos-message"></a>\_Message GETPOS UDM

Récupère la position actuelle d’un contrôle up-up avec une précision de 16 bits.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) a la valeur zéro et [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est défini à la position actuelle du contrôle. Si une erreur se produit, **HIWORD** est défini sur une valeur différente de zéro.

## <a name="remarks"></a>Notes

Lors du traitement de ce message, le contrôle up-up met à jour sa position actuelle en fonction de la légende de la fenêtre associée. Le contrôle up-up retourne une erreur s’il n’existe aucune fenêtre associée ou si la légende spécifie une valeur non valide ou hors limites. En outre, un indicateur d’erreur est défini dans le HIWORD du retour si le contrôle est créé sans le style [**uds \_ SETBUDDYINT**](up-down-control-styles.md) , même s’il retourne une valeur position valide dans le LOWORD du retour.

Si les valeurs 32 bits ont été activées pour un contrôle up-UpDown avec [**UDM \_ SETRANGE32**](udm-setrange32.md), ce message retourne uniquement les 16 bits inférieurs de la position. Pour récupérer la position 32 bits complète, utilisez [**UDM \_ GETPOS32**](udm-getpos32.md).

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

[**\_GETRANGE UDM**](udm-getrange.md)
</dt> <dt>

[**\_GETRANGE32 UDM**](udm-getrange32.md)
</dt> <dt>

[**\_SetPos UDM**](udm-setpos.md)
</dt> <dt>

[**\_SETRANGE32 UDM**](udm-setrange32.md)
</dt> </dl>

 

