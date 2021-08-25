---
title: Message TTM_GETTITLE (commctrl. h)
description: Récupérez les informations relatives au titre d’un contrôle ToolTip.
ms.assetid: d8992dd1-1610-44e8-8c0f-8ae1ac4b5898
keywords:
- TTM_GETTITLE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TTM_GETTITLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 242e20f3360caac03874524df38267fc0b103ec8f1c04d8d30df106fc9c65ac4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797439"
---
# <a name="ttm_gettitle-message"></a>\_Message atténuation GETTITLE

Récupérez les informations relatives au titre d’un contrôle ToolTip.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TTGETTITLE**](/windows/desktop/api/Commctrl/ns-commctrl-ttgettitle) qui contient des informations sur un titre d’info-bulle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour n’est pas utilisée.

## <a name="remarks"></a>Remarques

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





