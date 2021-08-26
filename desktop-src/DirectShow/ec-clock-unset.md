---
description: Le fournisseur d’horloge a été déconnecté.
ms.assetid: 0a885b7a-840d-4112-85f7-ff6f2d87bb75
title: EC_CLOCK_UNSET (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd7bc9daecb9e39ca2d121c9fa903b2e4e8257e6247f28d718ca093b302cc2e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998219"
---
# <a name="ec_clock_unset"></a>horloge EC non \_ \_ définie

Le fournisseur d’horloge a été déconnecté.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Zéro.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

le gestionnaire de Graph de filtre choisit une nouvelle horloge de référence lors de la prochaine pause ou de la commande run. Il transfère également l’événement à l’application.

## <a name="remarks"></a>Remarques

KSProxy signale cet événement lorsque le pin d’un filtre fournissant des horloges est déconnecté.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes de notification d’événement](event-notification-codes.md)
</dt> <dt>

[Notification d’événements dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




