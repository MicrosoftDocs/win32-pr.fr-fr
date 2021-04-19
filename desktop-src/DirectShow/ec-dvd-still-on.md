---
description: Signale le début de tout toujours (PGC, Cell ou VOBU).
ms.assetid: cf2b08c9-22fa-4559-9289-787eaec46c6c
title: EC_DVD_STILL_ON (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_STILL_ON
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0e2f9fcfecc44ee6d0769e00805c0aee512b2e7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520828"
---
# <a name="ec_dvd_still_on"></a>\_DVD EC \_ toujours \_ allumé

Signale le début de tout toujours (PGC, Cell ou VOBU).

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valeur booléenne (**bool**) indiquant si des boutons sont disponibles. Zéro (0) indique que les boutons sont disponibles, de sorte que la méthode [**IDvdControl2 :: StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) ne fonctionnera pas. Un (1) indique qu’aucun bouton n’est disponible. par conséquent, **IDvdControl2 :: StillOff** fonctionne.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valeur **DWORD** indiquant le nombre de secondes restantes de la dernière opération. 0xFFFFFFFF indique qu’il s’agit toujours d’un infini, ce qui signifie que l’utilisateur appuie sur un bouton ou jusqu’à ce que l’application appelle [**IDvdControl2 :: StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff).

</dd> </dl>

## <a name="remarks"></a>Notes

Toutes les combinaisons de boutons et sont toujours possibles (les boutons activés sont toujours activés, les boutons activés sont toujours désactivés, le bouton désactivé est toujours activé et le bouton désactivé est désactivé).

Cet événement est déclenché dans tous les domaines.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Dvdevcode. h (inclure DShow. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> <dt>

[Codes de notification des événements DVD](dvd-notification-codes.md)
</dt> <dt>

[Notification d’événement dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




