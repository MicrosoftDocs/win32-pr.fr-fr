---
title: Message LVM_MAPINDEXTOID (commctrl. h)
description: Cartes l’index d’un élément à un ID unique.
ms.assetid: d0486e21-2703-4289-abb0-f5f9c7b60b40
keywords:
- LVM_MAPINDEXTOID les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_MAPINDEXTOID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 254bfff0ee1598b0657b44a967b9e1331b076a462c8703855c5dd23109a8835d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958148"
---
# <a name="lvm_mapindextoid-message"></a>\_Message MAPINDEXTOID LVM

Cartes l’index d’un élément à un ID unique.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index d’un élément.

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un ID unique.

## <a name="remarks"></a>Remarques

Les contrôles List-View effectuent le suivi interne des éléments par index. Cela peut présenter des problèmes, car les index peuvent changer pendant la durée de vie du contrôle.

Le contrôle List-View peut baliser un élément avec un ID lors de la création de l’élément. Vous pouvez utiliser cet ID pour garantir l’unicité pendant la durée de vie du contrôle List-View.

Pour identifier un élément de manière unique, prenez l’index retourné à partir d’un appel tel que [**IComponent :: GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) et appelez **LVM \_ MAPINDEXTOID**. La valeur de retour est un ID unique.

> [!Note]  
> Dans un environnement multithread, l’index est garanti uniquement sur le thread qui héberge le contrôle List-View, et non sur les threads d’arrière-plan.

 

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

