---
title: Message TB_GETMETRICS (commctrl. h)
description: Récupère les métriques d’un contrôle ToolBar.
ms.assetid: 19c735cf-09f8-443e-8a73-dd64af0193a1
keywords:
- TB_GETMETRICS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_GETMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 733932b28dce34d06df0cbfc1d704763401b36a68380dc0aa8958b9bc3aff32f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078343"
---
# <a name="tb_getmetrics-message"></a>TO \_ GETMETRICS message

Récupère les métriques d’un contrôle ToolBar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) qui reçoit les métriques de barre d’outils.

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



 

 





