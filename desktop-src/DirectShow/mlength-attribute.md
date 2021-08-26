---
description: L’attribut mlength spécifie la durée d’un fichier source. Cette valeur doit être la durée réelle ou des erreurs de rendu peuvent se produire.
ms.assetid: f33ce85c-df61-4248-8dea-677162fa1a07
title: Attribut mlength
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2aac65cd917fe99e296298bac425e0ff76ca18fc51c82e9294eaedf0ef1c23c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051149"
---
# <a name="mlength-attribute"></a>Attribut mlength

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

L' `mlength` attribut spécifie la durée d’un fichier source. Cette valeur doit être la durée réelle ou des erreurs de rendu peuvent se produire.

## <a name="applies-to"></a>S'applique à

[**capture**](clip-element.md)

## <a name="possible-values"></a>Valeurs possibles

Doit être une chaîne au format *hh : mm : SS. FF* , où *hh* = heures, *mm* = minutes, *SS* = secondes et *FF* = fractions de secondes. Exemple : 1:04:30.512. Les unités de début peuvent être omises. Par exemple, 3:00 (trois minutes) et 45 (45 secondes) sont valides.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Attributs XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md)
</dt> </dl>

 

 



