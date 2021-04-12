---
title: Message LVM_GETGROUPINFOBYINDEX (commctrl. h)
description: Obtient des informations sur un groupe spécifié. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView GetGroupInfoByIndex.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getgroupinfobyindex.htm
keywords:
- LVM_GETGROUPINFOBYINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFOBYINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff801eae55ab4b4194ef23e624ff6eff75fbc25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104458"
---
# <a name="lvm_getgroupinfobyindex-message"></a>\_Message GETGROUPINFOBYINDEX LVM

Obtient des informations sur un groupe spécifié. Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ GetGroupInfoByIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Index du groupe.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Pointeur vers une structure [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) pour recevoir des informations sur le groupe spécifié par *wParam*. Le processus appelant est chargé d’allouer de la mémoire pour la structure et toutes les mémoires tampons de la structure, telles que celle sur laquelle pointe le membre **pszHeader** . Définissez tous les membres conditionnels de la structure, tels que **cchHeader** , la taille de la mémoire tampon vers laquelle pointe **pszHeader** dans **WCHARs** , y compris le caractère **null** de fin. Définissez **cbSize** sur sizeof (LVGROUP).

Le récepteur de messages est chargé de définir les membres de structure avec les informations relatives au groupe spécifié par *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





