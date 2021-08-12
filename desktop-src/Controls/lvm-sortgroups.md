---
title: Message LVM_SORTGROUPS (commctrl. h)
description: Utilise une fonction de comparaison définie par l’application pour trier des groupes par ID au sein d’un contrôle List-View.
ms.assetid: 553e96d6-a982-4482-8fba-ef11a74fb82e
keywords:
- LVM_SORTGROUPS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_SORTGROUPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ec17d46205746495cfe95a2af83690644dd8bfced26041906bdea4f809fb36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670783"
---
# <a name="lvm_sortgroups-message"></a>\_Message SORTGROUPS LVM

Utilise une fonction de comparaison définie par l’application pour trier des groupes par ID au sein d’un contrôle List-View.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Pointeur vers une fonction de comparaison définie par l’application, <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">LVGroupCompare</a>.</dd> <dt>

*lParam* 
</dt> <dd>Pointeur void vers les informations définies par l’application.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 1 en cas de réussite, ou 0 dans le cas contraire.

## <a name="remarks"></a>Remarques

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> </dl>

