---
title: Message TB_GETBITMAPFLAGS (commctrl. h)
description: Récupère les indicateurs qui décrivent le type de bitmap à utiliser.
ms.assetid: 64a66fe6-1446-424c-a0c6-388da6a7b081
keywords:
- TB_GETBITMAPFLAGS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_GETBITMAPFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b9bce2f6e9bf862b10b162bf9172c0144d15c07328b61cbdb79bcf05c759e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670027"
---
# <a name="tb_getbitmapflags-message"></a>TO \_ GETBITMAPFLAGS message

Récupère les indicateurs qui décrivent le type de bitmap à utiliser.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **DWORD** qui décrit le type de bitmap à utiliser. Si la valeur de retour est définie sur l' \_ indicateur TBBF large, les applications doivent utiliser des bitmaps de grande taille (24 x 24); dans le cas contraire, les applications doivent utiliser de petites bitmaps (16 x 16). Tous les autres bits sont réservés.

## <a name="remarks"></a>Remarques

La valeur retournée par **to \_ GETBITMAPFLAGS** est uniquement consultative. Le contrôle ToolBar recommande des bitmaps de grande taille ou de petite taille selon que l’utilisateur a choisi des polices de grande taille ou de petite taille.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





