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
ms.openlocfilehash: 7900aadf3ba87cc7603a3fe15f4974911c9f9a37
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123913"
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

## <a name="return-value"></a>Valeur de retour

La valeur de retour est le nombre d’éléments dans la zone de liste. Si une erreur se produit, il s’agit de CB \_ Err.

## <a name="remarks"></a>Notes

L’index est de base zéro, le nombre retourné est donc supérieur à la valeur d’index du dernier élément.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



 

 





