---
title: Message LVM_SETITEMINDEXSTATE (commctrl. h)
description: Définit l’état d’un élément de vue liste. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView SetItemIndexState.
ms.assetid: 9fea6420-320a-4d2a-84b5-7923fbb14655
keywords:
- LVM_SETITEMINDEXSTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMINDEXSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ce8f6847c733127053e2162dd785d52fb77cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032619"
---
# <a name="lvm_setitemindexstate-message"></a>\_Message SETITEMINDEXSTATE LVM

Définit l’état d’un élément de vue liste. Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ SetItemIndexState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) pour l’élément. Le processus appelant est chargé d’allouer cette structure et de définir les membres.

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . Le processus appelant est chargé d’allouer de la mémoire pour la structure. Définissez le membre d' **État** sur une ou plusieurs (combinaison d’opérations de bits) des indicateurs d' [État d’élément de liste](list-view-item-states.md) . Définissez le membre **stateMask** de la structure pour indiquer les bits valides du membre d' **État** . Pour plus d’informations, consultez le membre **stateMask** de la structure **LVITEM** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs suivantes de type **HRESULT**.



| Code de retour                                                                                  | Description                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**E \_ échec**</dt> </dl>       | Impossible de définir l’État.<br/>                            |
| <dl> <dt>**E \_ inattendu**</dt> </dl> | Le contrôle List-View n’était pas prêt pour l’opération.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>         | L'opération a réussi.<br/>                          |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





