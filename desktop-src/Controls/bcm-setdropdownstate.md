---
title: Message BCM_SETDROPDOWNSTATE (commctrl. h)
description: Définit l’État déroulant d’un bouton avec la \_ liste déroulante style TBSTYLE. Envoyez ce message explicitement ou à l’aide de la \_ macro Button SetDropDownState.
ms.assetid: 725deff4-0bcb-497d-a6cf-e9c98b05f16e
keywords:
- BCM_SETDROPDOWNSTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- BCM_SETDROPDOWNSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc44ec58d40e047708591121f81c84f327ca47c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103633"
---
# <a name="bcm_setdropdownstate-message"></a>\_Message SETDROPDOWNSTATE BCM

Définit l’État déroulant d’un bouton avec la [**\_ liste déroulante style TBSTYLE**](toolbar-control-and-button-styles.md). Envoyez ce message explicitement ou à l’aide de la macro [**Button \_ SetDropDownState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Valeur **booléenne** qui est **true** pour l’état de BST \_ DROPDOWNPUSHED, ou **false** dans le cas contraire.

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

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

[Styles de bouton](button-styles.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Types de bouton](button-types-and-styles.md)
</dt> </dl>

 

 





