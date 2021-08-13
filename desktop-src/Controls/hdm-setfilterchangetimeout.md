---
title: Message HDM_SETFILTERCHANGETIMEOUT (commctrl. h)
description: Définit l’intervalle de délai d’attente entre le moment où une modification est effectuée dans les attributs de filtre et la publication d’une \_ notification HDN FILTERCHANGE. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ SetFilterChangeTimeout.
ms.assetid: 9bc8e0e7-d7c1-4dd6-9d39-6ae937f19d60
keywords:
- HDM_SETFILTERCHANGETIMEOUT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- HDM_SETFILTERCHANGETIMEOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b5f8df12a7f30baa5f8b7d4bf15698b30cfbb6619fb71a81d4977b259c318b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435859"
---
# <a name="hdm_setfilterchangetimeout-message"></a>\_Message HDM SETFILTERCHANGETIMEOUT

Définit l’intervalle de délai d’attente entre le moment où une modification est effectuée dans les attributs de filtre et la publication d’une notification [HDN \_ FILTERCHANGE](hdn-filterchange.md) . Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ SetFilterChangeTimeout**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Valeur du délai d'attente, en millisecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index du contrôle de filtre en cours de modification.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[HDN \_ FILTERCHANGE](hdn-filterchange.md)
</dt> </dl>

 

 





