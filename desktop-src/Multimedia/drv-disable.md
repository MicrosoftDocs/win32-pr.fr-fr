---
title: Message DRV_DISABLE (mmsystem. h)
description: Désactive le pilote. Le pilote doit placer l’appareil correspondant, le cas échéant, dans un état inactif et terminer les fonctions de rappel ou les threads.
ms.assetid: 83e99397-6f0e-4174-9f96-e10c1f17ef0b
keywords:
- Message DRV_DISABLE Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_DISABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b512e90612a02681008474c7f1323f17304422d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942828"
---
# <a name="drv_disable-message"></a>DRV- \_ message de désactivation

Désactive le pilote. Le pilote doit placer l’appareil correspondant, le cas échéant, dans un état inactif et terminer les fonctions de rappel ou les threads.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Handle de l’instance du pilote installable.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Les paramètres *dwDriverId*, *lParam1* et *lParam2* ne sont pas utilisés.

Après la désactivation du pilote, le système envoie généralement au pilote un message de fin de la commande [**DRV \_**](drv-free.md) avant de supprimer le pilote de la mémoire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>MMSYSTEM. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Pilotes installables](installable-drivers.md)
</dt> <dt>

[Messages de pilote installables](installable-driver-messages.md)
</dt> </dl>

 

 





