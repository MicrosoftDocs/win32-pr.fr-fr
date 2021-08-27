---
title: Message LVM_MAPIDTOINDEX (commctrl. h)
description: Cartes l’ID d’un élément à un index.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_mapidtoindex.htm
keywords:
- LVM_MAPIDTOINDEX les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_MAPIDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77b5380d52f839f28324b808ed0d3304b6c5e2837869e0f0cfc6ab99d8f00b04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079869"
---
# <a name="lvm_mapidtoindex-message"></a>\_Message MAPIDTOINDEX LVM

Cartes l’ID d’un élément à un index.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

ID unique d’un élément.

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index le plus récent.

## <a name="remarks"></a>Remarques

Les contrôles List-View effectuent le suivi interne des éléments par index. Cela peut présenter des problèmes, car les index peuvent changer pendant la durée de vie du contrôle.

Le contrôle List-View peut baliser un élément avec un ID lors de la création de l’élément. Vous pouvez utiliser cet ID pour garantir l’unicité pendant la durée de vie du contrôle List-View.

Pour identifier un élément de manière unique, prenez l’index retourné à partir d’un appel tel que [**IComponent :: GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) et appelez [**LVM \_ MAPINDEXTOID**](lvm-mapindextoid.md). La valeur de retour est un ID unique.

Si vous avez besoin de l’index d’un élément après la création d’un ID, vous pouvez appeler **LVM \_ MAPIDTOINDEX** avec l’ID unique et il retourne l’index le plus récent.

**LVM \_ MAPIDTOINDEX** n’est pas pris en charge sous le style [**\_ OWNERDATA LVS**](list-view-window-styles.md) .

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



 

