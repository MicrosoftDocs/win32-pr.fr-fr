---
description: Un nouveau segment a démarré.
ms.assetid: 9742436a-e233-4641-a0d5-aa240cde5f28
title: EC_SEGMENT_STARTED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e7df85bddb78fe2687a017b481e6db62ba37c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528407"
---
# <a name="ec_segment_started"></a>\_segment EC \_ démarré

Un nouveau segment a démarré.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**const** **Reference \_ Time** \* ) pointeur vers une valeur de **\_ temps de référence** qui spécifie le temps de flux cumulé depuis le début du segment, en unités de 100 nanosecondes.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) Numéro de segment (de base zéro).

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Cet événement n’est pas envoyé à l’application. Les applications ne peuvent pas remplacer l’action par défaut pour cet événement.

## <a name="remarks"></a>Notes

Si un filtre envoie une [**\_ fin \_ de \_ segment ce**](ec-end-of-segment.md) à la fin d’un segment, il envoie cet événement au début du segment. Le gestionnaire de graphique de filtre utilise cette notification d’événement pour calculer le \_ nombre \_ de \_ notifications de la fin de segment qu’il doit attendre à la fin du segment.

Par défaut, les filtres n’envoient pas d’événements [**\_ \_ de fin de \_ segment EC**](ec-end-of-segment.md) à la fin des segments et ne doivent donc pas envoyer cet événement. Pour plus d’informations, consultez [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes de notification d’événement](event-notification-codes.md)
</dt> <dt>

[Notification d’événement dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




