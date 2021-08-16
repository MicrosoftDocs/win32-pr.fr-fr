---
title: Message CB_GETCOUNT (winuser. h)
description: Obtient le nombre d’éléments dans la zone de liste d’une zone de liste déroulante.
ms.assetid: 69667724-5452-4fcc-afc3-0d98d3beedc8
keywords:
- CB_GETCOUNT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8215046ae9558fd03388b2b0637233c2f69832ea07a7f20fd24ddc0a5eb3c177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832277"
---
# <a name="cb_getcount-message"></a>\_Message CB GETCOUNT

Obtient le nombre d’éléments dans la zone de liste d’une zone de liste déroulante.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est le nombre d’éléments dans la zone de liste. Si une erreur se produit, il s’agit de CB \_ Err.

## <a name="remarks"></a>Remarques

L’index est de base zéro, le nombre retourné est donc supérieur à la valeur d’index du dernier élément.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



 

 





