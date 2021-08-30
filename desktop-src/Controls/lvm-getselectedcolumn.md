---
title: Message LVM_GETSELECTEDCOLUMN (commctrl. h)
description: Récupère un entier qui spécifie la colonne sélectionnée.
ms.assetid: 5aba5d96-50fd-439b-9782-fd5d8684b17f
keywords:
- LVM_GETSELECTEDCOLUMN les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETSELECTEDCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d17cb13a98493022b81a86485422e0021b86605bb45bd757067d1d1c9050d92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968259"
---
# <a name="lvm_getselectedcolumn-message"></a>\_Message GETSELECTEDCOLUMN LVM

Récupère un entier qui spécifie la colonne sélectionnée.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un **uint** qui spécifie la colonne sélectionnée.

## <a name="remarks"></a>Remarques

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





