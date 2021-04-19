---
title: Message CBEM_SETEXTENDEDSTYLE (commctrl. h)
description: Définit des styles étendus dans un contrôle ComboBoxEx.
ms.assetid: 00848bd0-5a2f-4bfb-ae1f-ee3aa88ac57a
keywords:
- CBEM_SETEXTENDEDSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- CBEM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a60518d2f6130c2c89e379125308fc2e647c6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513640"
---
# <a name="cbem_setextendedstyle-message"></a>\_Message CBEM SETEXTENDEDSTYLE

Définit des styles étendus dans un contrôle ComboBoxEx.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur **DWORD** qui indique les styles de *lParam* à affecter. Seuls les styles étendus dans *wParam* seront modifiés. Si ce paramètre est égal à zéro, tous les styles de *lParam* sont affectés.

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur **DWORD** qui contient les [styles étendus de contrôle ComboBoxEx](comboboxex-control-extended-styles.md) à définir pour le contrôle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **DWORD** qui contient les styles étendus utilisés précédemment pour le contrôle.

## <a name="remarks"></a>Notes

*wParam* vous permet de modifier un ou plusieurs styles étendus sans avoir à récupérer d’abord les styles existants. Par exemple, si vous transmettez [**CBES \_ ex \_ NOEDITIMAGE**](comboboxex-control-extended-styles.md) pour *wParam* et 0 pour *lParam*, le style **CBES \_ ex \_ NOEDITIMAGE** sera effacé, mais tous les autres styles resteront les mêmes.

Si vous essayez de définir un style étendu pour un contrôle ComboBoxEx créé avec le style [**CBS \_ simple**](combo-box-styles.md) , il se peut qu’il ne redessine pas correctement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





