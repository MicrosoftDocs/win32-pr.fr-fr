---
title: Message CBEM_GETEDITCONTROL (commctrl. h)
description: Obtient le handle vers la partie du contrôle d’édition d’un contrôle ComboBoxEx. Un contrôle ComboBoxEx utilise une zone d’édition quand il est défini sur le \_ style de liste déroulante CBS.
ms.assetid: def91949-cadc-4297-a504-0680d7d9b815
keywords:
- CBEM_GETEDITCONTROL les contrôles de message Windows
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
ms.openlocfilehash: 412d1183b29c8c89b5977d5f7f2a1b962d54dc01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105598"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





