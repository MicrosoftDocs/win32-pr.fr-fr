---
title: Message LM_SETITEM (commctrl. h)
description: Définit les États et les attributs d’un élément.
ms.assetid: 02a68a31-2541-480e-b768-449d40e5e9e0
keywords:
- LM_SETITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LM_SETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8dccdb37536352c8783f7dd6af6a9475f5bea69111e2f7f09e5395b0ebf25b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062799"
---
# <a name="lm_setitem-message"></a>\_Message LM SETITEM

Définit les États et les attributs d’un élément.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit avoir la **valeur null**. </dd> <dt>

*lParam* 
</dt> <dd>Pointeur vers une structure <a href="/windows/win32/api/commctrl/ns-commctrl-litem">litem</a> contenant les nouveaux États et attributs souhaités pour le lien. </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si le message parvient à la définition des valeurs et des attributs spécifiés.

## <a name="remarks"></a>Remarques

Avec le message [**LM \_ GETITEM**](lm-getitem.md) , les liens sont accessibles uniquement par le biais de l’index numérique renvoyé dans le membre **iLink** de [**litem**](/windows/win32/api/commctrl/ns-commctrl-litem). L’accès au lien via le nom d’ID renvoyé dans **szID** n’est pas pris en charge.

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comctl32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





