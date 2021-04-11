---
title: Message RB_SETWINDOWTHEME (commctrl. h)
description: Définit le style visuel d’un contrôle rebar.
ms.assetid: 5b32b354-3e25-4d02-9334-cc57acf41a73
keywords:
- RB_SETWINDOWTHEME les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e136562394d26dd56d8d4c0c9ae916948144dbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104779"
---
# <a name="rb_setwindowtheme-message"></a>\_Message SETWINDOWTHEME RB

Définit le style visuel d’un contrôle rebar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une chaîne Unicode qui contient le style visuel rebar à définir.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour n’est pas utilisée.

## <a name="remarks"></a>Notes

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





