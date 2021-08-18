---
description: L’attribut mstop spécifie l’heure d’arrêt d’un clip, par rapport au fichier multimédia d’origine.
ms.assetid: 01559d29-9c7b-4842-a1f7-16552adbda43
title: Attribut mstop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d432c3ed9ff80a9252def74fb553ed307668b36e660d96963baae0f4d0db04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072935"
---
# <a name="mstop-attribute"></a>Attribut mstop

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

L' `mstop` attribut spécifie l’heure d’arrêt d’un clip, par rapport au fichier multimédia d’origine.

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

 

 



