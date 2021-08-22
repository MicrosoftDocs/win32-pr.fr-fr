---
title: Message CBEM_SETEXTENDEDSTYLE (commctrl. h)
description: Définit des styles étendus dans un contrôle ComboBoxEx.
ms.assetid: 00848bd0-5a2f-4bfb-ae1f-ee3aa88ac57a
keywords:
- CBEM_SETEXTENDEDSTYLE les contrôles de Windows de message
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
ms.openlocfilehash: efd1083e838d85f9cb659acb9a28b74a1d8605934be4c53fd72993e7470fad2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527969"
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

## <a name="remarks"></a>Remarques

*wParam* vous permet de modifier un ou plusieurs styles étendus sans avoir à récupérer d’abord les styles existants. Par exemple, si vous transmettez [**CBES \_ ex \_ NOEDITIMAGE**](comboboxex-control-extended-styles.md) pour *wParam* et 0 pour *lParam*, le style **CBES \_ ex \_ NOEDITIMAGE** sera effacé, mais tous les autres styles resteront les mêmes.

Si vous essayez de définir un style étendu pour un contrôle ComboBoxEx créé avec le style [**CBS \_ simple**](combo-box-styles.md) , il se peut qu’il ne redessine pas correctement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





