---
title: Message DRV_EXITSESSION (mmsystem. h)
description: informe le pilote que Windows se prépare à quitter. Le pilote doit se préparer à l’arrêt.
ms.assetid: 8d200d64-b89b-47f1-ad21-ab86987efa4b
keywords:
- message DRV_EXITSESSION Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_EXITSESSION
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236da457541af2d594bc708caf5b5ed07e58cc04
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364148"
---
# <a name="drv_exitsession-message"></a>\_Message EXITSESSION

informe le pilote que Windows se prépare à quitter. Le pilote doit se préparer à l’arrêt.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*
</dt> <dd>

Identificateur du pilote installable. Il s’agit de la même valeur que celle précédemment retournée par le pilote à partir du message de l' [**\_ ouverture du DRV**](drv-open.md) .

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Handle de l’instance du pilote installable.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Les paramètres *lParam1* et *lParam2* ne sont pas utilisés.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Mmsystem. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Pilotes installables](installable-drivers.md)
</dt> <dt>

[Messages de pilote installables](installable-driver-messages.md)
</dt> </dl>

 

 





