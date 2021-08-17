---
title: Message LVM_GETGROUPINFO (commctrl. h)
description: Obtient les informations de groupe.
ms.assetid: 72d84e0b-121e-473b-a34d-874234c598b6
keywords:
- LVM_GETGROUPINFO les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5c48a21a1bba0c6dd1af3fd567ea853dc922591c553ea11a935fb705ad65bf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411393"
---
# <a name="lvm_getgroupinfo-message"></a>\_Message GETGROUPINFO LVM

Obtient les informations de groupe.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>ID qui spécifie le groupe dont les informations sont récupérées.</dd> <dt>

*lParam* 
</dt> <dd>Pointeur une structure <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> qui reçoit les informations récupérées. Définissez le membre **cbSize** de cette structure sur sizeof (LVGROUP). </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’ID du groupe en cas de réussite, ou-1 dans le cas contraire.

## <a name="remarks"></a>Remarques

Avant de tenter de récupérer l’en-tête d’un groupe, assurez-vous d’abord que le groupe n’a pas le \_ style d’en-tête LBGS.

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





