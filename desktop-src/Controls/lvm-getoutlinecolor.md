---
title: Message LVM_GETOUTLINECOLOR (commctrl. h)
description: Récupère la couleur de la bordure d’un contrôle List View si le \_ \_ style de fenêtre étendue LVS ex BORDERSELECT est défini.
ms.assetid: cc9d69d1-1470-4eaa-8d54-e31b796cf685
keywords:
- LVM_GETOUTLINECOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489f21f2f6d4dcca2c79d92a13a85d7718a85693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844094"
---
# <a name="lvm_getoutlinecolor-message"></a>\_Message GETOUTLINECOLOR LVM

Récupère la couleur de la bordure d’un contrôle List View si le style de fenêtre étendue [**LVS \_ ex \_ BORDERSELECT**](extended-list-view-styles.md) est défini.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une structure **COLORREF** qui contient la couleur de la bordure d’un contrôle List View.

## <a name="remarks"></a>Notes

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





