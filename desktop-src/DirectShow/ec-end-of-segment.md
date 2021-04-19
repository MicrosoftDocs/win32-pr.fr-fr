---
description: La fin d’un segment a été atteinte.
ms.assetid: 07f141b1-2e96-49e2-9cf7-581690e245b5
title: EC_END_OF_SEGMENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a779b0f46a031ad694bd3fed3fe29536424a3a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534986"
---
# <a name="ec_end_of_segment"></a>\_fin \_ de \_ segment ce

La fin d’un segment a été atteinte.

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

Le gestionnaire de graphes de filtre vérifie le nombre d’événements de la **\_ fin ce \_ du \_ segment** par rapport au nombre d’événements de [**\_ \_ début de segment EC**](ec-segment-started.md) . S’ils correspondent, il transfère l’événement **\_ de fin \_ de \_ segment EC** à l’application. Les applications ne peuvent pas remplacer l’action par défaut pour cet événement.

## <a name="remarks"></a>Notes

Ce code d’événement prend en charge le bouclage transparent. Lorsqu’un appel à la méthode [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) comprend l' \_ indicateur AM chercher le \_ segment, le filtre source envoie ce code d’événement au lieu d’appeler [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream).

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

 

 




