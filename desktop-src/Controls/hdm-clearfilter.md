---
title: Message HDM_CLEARFILTER (commctrl. h)
description: Efface le filtre pour un contrôle d’en-tête donné. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ ClearFilter.
ms.assetid: 74c0265e-68d1-4414-8fd9-20f5f041d4b4
keywords:
- HDM_CLEARFILTER les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_CLEARFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b1184432517761a567cd76bdd488e4593b1e999
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104491"
---
# <a name="hdm_clearfilter-message"></a>\_Message HDM CLEARFILTER

Efface le filtre pour un contrôle d’en-tête donné. Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur de colonne indiquant le filtre à effacer.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un entier. La propriété **LRESULT** est castée en un entier qui indique **true**(1) ou **false**(0).

## <a name="remarks"></a>Notes

Si la valeur de colonne est définie sur-1, tous les filtres sont effacés et la notification [ \_ FILTERCHANGE HDN](hdn-filterchange.md) n’est envoyée qu’une seule fois.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ClearAllFilters d’en-tête \_**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)
</dt> </dl>

 

 





