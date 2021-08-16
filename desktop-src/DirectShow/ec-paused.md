---
description: Une demande de suspension est terminée.
ms.assetid: 32acad47-65bd-42f0-987e-3690bb824b05
title: EC_PAUSED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebc16eefcf88402ccf0a6173bcfa22e3100c33985469b7372ad6bb2ea97c572d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820050"
---
# <a name="ec_paused"></a>en \_ Pause EC

Une demande de suspension est terminée.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) État de la pause opération.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Aucun.

## <a name="remarks"></a>Notes

Le gestionnaire de graphique de filtre envoie cet événement lorsqu’il termine une commande de suspension asynchrone.

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

 

 




