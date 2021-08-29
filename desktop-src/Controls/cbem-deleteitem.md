---
title: Message CBEM_DELETEITEM (commctrl. h)
description: Supprime un élément d’un contrôle ComboBoxEx.
ms.assetid: 688cf388-54ba-4b45-88d7-628da49d8615
keywords:
- CBEM_DELETEITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CBEM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afba180ad6b714b597fe688cbaf1496b92735d8924cd6a238d56f081753fb3e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063308"
---
# <a name="cbem_deleteitem-message"></a>\_Message CBEM DELETEITEM

Supprime un élément d’un contrôle ComboBoxEx.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de l’élément à supprimer.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur INT qui représente le nombre d’éléments restants dans le contrôle. Si *iIndex* n’est pas valide, le message retourne CB \_ Err.

## <a name="remarks"></a>Remarques

Ce message est mappé au message de contrôle de zone de liste déroulante [**CB \_ DELETESTRING**](cb-deletestring.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





