---
title: Message LVM_GETINSERTMARKRECT (commctrl. h)
description: Récupère le rectangle qui délimite le point d’insertion.
ms.assetid: 7b10229c-73ab-426c-8a8a-71258a33e248
keywords:
- LVM_GETINSERTMARKRECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARKRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5832ce185a579432b341482847400e96d60869a64d3ff0a2cd599e2eecf6b20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062599"
---
# <a name="lvm_getinsertmarkrect-message"></a>\_Message GETINSERTMARKRECT LVM

Récupère le rectangle qui délimite le point d’insertion.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Non utilisé ; doit être égal à zéro.</dd> <dt>

*lParam* 
</dt> <dd>Pointeur vers une structure <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> qui contient les coordonnées d’un rectangle qui délimite le point d’insertion.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs suivantes.



| Code de retour                                                                      | Description                          |
|----------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**entre**</dt> </dl> | Aucun point d’insertion trouvé.<br/> |
| <dl> <dt>**1**</dt> </dl> | Point d’insertion trouvé.<br/>    |



 

## <a name="remarks"></a>Remarques

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

