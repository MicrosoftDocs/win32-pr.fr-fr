---
description: L’attribut mstart spécifie l’heure de début d’un clip, par rapport au fichier multimédia d’origine.
ms.assetid: ed63f448-8ca3-4733-afc0-2d743f82bebe
title: Attribut mstart
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c65ffcb7d3da41f3e1f1232e37a6f5786755980eb63a8bbc554bbe726f453e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050949"
---
# <a name="mstart-attribute"></a>Attribut mstart

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

L' `mstart` attribut spécifie l’heure de début d’un clip, par rapport au fichier multimédia d’origine.

## <a name="applies-to"></a>S'applique à

[**capture**](clip-element.md)

## <a name="possible-values"></a>Valeurs possibles

Doit être une chaîne au format *hh : mm : SS. FF* , où *hh* = heures, *mm* = minutes, *SS* = secondes et *FF* = fractions de secondes. Exemple : 1:04:30.512. Les unités de début peuvent être omises. Par exemple, 3:00 (trois minutes) et 45 (45 secondes) sont valides.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Attributs XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



