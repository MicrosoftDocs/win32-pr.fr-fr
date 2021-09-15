---
title: Message LVM_SETTILEVIEWINFO (commctrl. h)
description: Définit les informations qu’un contrôle List View utilise en mode mosaïque.
ms.assetid: 1c4f2aff-1ce1-484a-9360-3efbe870b39b
keywords:
- LVM_SETTILEVIEWINFO les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_SETTILEVIEWINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25d6c728d92bb931837eca440af679b5bcb98d1e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312629"
---
# <a name="lvm_settileviewinfo-message"></a>\_Message SETTILEVIEWINFO LVM

Définit les informations qu’un contrôle List View utilise en mode mosaïque.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Pointeur vers une structure <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> qui contient les informations à définir.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





