---
title: Message LVM_INSERTMARKHITTEST (commctrl. h)
description: Récupère le point d’insertion le plus proche d’un point spécifié.
ms.assetid: 901bb770-a36d-4d9f-a53b-d497b4df39e5
keywords:
- LVM_INSERTMARKHITTEST les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bdb82e924b4a5d74d152917f52c4039e0aca81b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105478"
---
# <a name="lvm_insertmarkhittest-message"></a>\_Message INSERTMARKHITTEST LVM

Récupère le point d’insertion le plus proche d’un point spécifié.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Pointeur vers une structure de **points** qui contient les coordonnées du test d’atteinte.</dd> <dt>

*lParam* 
</dt> <dd>Pointeur vers une structure <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> qui spécifie le point d’insertion le plus proche des coordonnées définies par le paramètre *wParam* .</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire. La **valeur false** est retournée si la taille du membre **cbSize** de la structure [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) n’est pas égale à la taille réelle de la structure, ou lorsqu’un point d’insertion ne s’applique pas à la vue actuelle.

## <a name="remarks"></a>Notes

Un point d’insertion ne peut apparaître que si le contrôle de liste est en mode icône, en mode petite icône ou en mode mosaïque et n’est pas en mode groupe.

Si les points d’insertion ne s’appliquent pas à la vue, la structure [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) contient-1 dans le membre **iItem** .

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





