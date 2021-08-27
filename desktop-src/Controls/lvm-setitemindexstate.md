---
title: Message LVM_SETITEMINDEXSTATE (commctrl. h)
description: Définit l’état d’un élément de vue liste. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView SetItemIndexState.
ms.assetid: 9fea6420-320a-4d2a-84b5-7923fbb14655
keywords:
- LVM_SETITEMINDEXSTATE les contrôles de Windows de message
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
ms.openlocfilehash: 18094986f5a57713e842b51b31c74ccfe4987d1c1fe62380ea8a986762e20c7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062209"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





