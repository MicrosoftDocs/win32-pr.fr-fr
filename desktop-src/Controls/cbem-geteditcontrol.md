---
title: Message CBEM_GETEDITCONTROL (commctrl. h)
description: Obtient le handle vers la partie du contrôle d’édition d’un contrôle ComboBoxEx. Un contrôle ComboBoxEx utilise une zone d’édition quand il est défini sur le \_ style de liste déroulante CBS.
ms.assetid: def91949-cadc-4297-a504-0680d7d9b815
keywords:
- CBEM_GETEDITCONTROL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CBEM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 885a90a1b37fab7cd8e4a492bd00ad349f96202e13ee25a404f7f4aa41f623e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118414069"
---
# <a name="cbem_geteditcontrol-message"></a>\_Message CBEM GETEDITCONTROL

Obtient le handle vers la partie du contrôle d’édition d’un contrôle ComboBoxEx. Un contrôle ComboBoxEx utilise une zone d’édition quand il est défini sur le style de [**\_ liste déroulante CBS**](combo-box-styles.md) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle du contrôle d’édition dans le contrôle ComboBoxEx s’il utilise le style de [**\_ liste déroulante CBS**](combo-box-styles.md) . Dans le cas contraire, le message retourne la **valeur null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





