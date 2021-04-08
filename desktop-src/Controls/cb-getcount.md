---
title: Message CB_GETCOUNT (winuser. h)
description: Obtient le nombre d’éléments dans la zone de liste d’une zone de liste déroulante.
ms.assetid: 69667724-5452-4fcc-afc3-0d98d3beedc8
keywords:
- CB_GETCOUNT les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103744020"
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

## <a name="remarks"></a>Notes

L’index est de base zéro, le nombre retourné est donc supérieur à la valeur d’index du dernier élément.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



 

 





