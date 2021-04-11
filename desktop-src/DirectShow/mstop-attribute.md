---
description: L’attribut mstop spécifie l’heure d’arrêt d’un clip, par rapport au fichier multimédia d’origine.
ms.assetid: 01559d29-9c7b-4842-a1f7-16552adbda43
title: Attribut mstop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a63f52a1b912392165293e008074cf64a03b9751
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108479"
---
# <a name="mstop-attribute"></a>Attribut mstop

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `mstop` attribut spécifie l’heure d’arrêt d’un clip, par rapport au fichier multimédia d’origine.

## <a name="applies-to"></a>S'applique à

[**clip**](clip-element.md)

## <a name="possible-values"></a>Valeurs possibles

Doit être une chaîne au format *hh : mm : SS. FF* , où *hh* = heures, *mm* = minutes, *SS* = secondes et *FF* = fractions de secondes. Exemple : 1:04:30.512. Les unités de début peuvent être omises. Par exemple, 3:00 (trois minutes) et 45 (45 secondes) sont valides.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Attributs XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



