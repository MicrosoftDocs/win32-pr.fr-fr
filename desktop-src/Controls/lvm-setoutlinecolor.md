---
title: Message LVM_SETOUTLINECOLOR (commctrl. h)
description: Définit la couleur de la bordure d’un contrôle d’affichage de liste si le \_ \_ style de fenêtre étendue LVS ex BORDERSELECT est défini.
ms.assetid: c2b606fa-8d47-4192-94b7-d01c3cfdc514
keywords:
- LVM_SETOUTLINECOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_SETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db9f5d53339ecec19fd6f06fcabd3a0471b1c3a569e8856571a98a99675a232
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119217389"
---
# <a name="lvm_setoutlinecolor-message"></a>\_Message SETOUTLINECOLOR LVM

Définit la couleur de la bordure d’un contrôle d’affichage de liste si le style de fenêtre étendue [**LVS \_ ex \_ BORDERSELECT**](extended-list-view-styles.md) est défini.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>**COLORREF** , structure qui spécifie la couleur de définition de la bordure.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la structure **COLORREF** qui contient la couleur de contour.

## <a name="remarks"></a>Remarques

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





