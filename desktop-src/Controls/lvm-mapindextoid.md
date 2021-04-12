---
title: Message LVM_MAPINDEXTOID (commctrl. h)
description: Mappe l’index d’un élément à un ID unique.
ms.assetid: d0486e21-2703-4289-abb0-f5f9c7b60b40
keywords:
- LVM_MAPINDEXTOID les contrôles de message Windows
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
ms.openlocfilehash: f6a2a5de558b025e61bef26fd20278f125372769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464890"
---
# <a name="lvm_mapindextoid-message"></a>\_Message MAPINDEXTOID LVM

Mappe l’index d’un élément à un ID unique.

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

## <a name="remarks"></a>Notes

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

