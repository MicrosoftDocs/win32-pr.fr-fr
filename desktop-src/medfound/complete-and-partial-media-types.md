---
description: Cette rubrique décrit la différence entre les types de médias complets et les types de média partiels.
ms.assetid: 59b3f0b5-f378-41e6-9b49-85a16bb6e008
title: Types de média complets et partiels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104f5509835c1f5f179c61b90f2c5f58636d022f4e5710b4b941e0819585fe85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958789"
---
# <a name="complete-and-partial-media-types"></a>Types de média complets et partiels

Cette rubrique décrit la différence entre les types de médias complets et les types de média partiels.

## <a name="complete-media-types"></a>Types de médias complets

Un type de média *complet* est un type qui définit complètement le format du flux multimédia. Étant donné un type de média complet, un composant de pipeline peut analyser les données de flux associées au type de média, sans ambiguïté.

Pour les formats non compressés, les rubriques suivantes définissent les attributs requis pour un type de média complet :

-   Audio : [types de média audio non compressés](uncompressed-audio-media-types.md)
-   Vidéo : [types de média vidéo non compressés](uncompressed-video-media-types.md)

Pour les flux compressés (ou *encodés*), la définition d’un type de média complet est définie par le codec. Toutefois, si des attributs de type non compressés sont connus pour le flux compressé, ces valeurs doivent être incluses dans le type de média du flux compressé. Par exemple, si la taille de trame est connue, définissez l’attribut de [**\_ \_ \_ taille de frame MT MF**](mf-mt-frame-size-attribute.md) sur le type de média, même si techniquement un flux compressé n’a pas de taille de trame.

## <a name="partial-media-types"></a>Types de média partiels

Un type de média *partiel* n’a pas un ou plusieurs des attributs nécessaires pour un type de média complet. Lors de l’énumération des types de média possibles, un composant Microsoft Media Foundation peut conserver une valeur non définie, pour indiquer qu’il peut gérer n’importe quelle valeur. Par exemple, un processeur vidéo peut conserver l’attribut de [**\_ fréquence d' \_ images \_ MF MT**](mf-mt-frame-rate-attribute.md) unset, pour indiquer qu’il peut gérer toute fréquence d’images, et effectuera une conversion de fréquence d’images si nécessaire.

Si vous créez un type de média partiel, vous devez toujours inclure autant d’informations que vous le savez. Toutefois, un type de média ne doit pas inclure d’informations incertaines. Il est préférable de ne pas avoir d’informations erronées.

Au minimum, un type de média partiel ne doit inclure que deux attributs : [**MF \_ MT \_ major \_ type**](mf-mt-major-type-attribute.md) et [**MF \_ MT \_ SubType**](mf-mt-subtype-attribute.md).

Parfois Media Foundation composants doivent fournir des types de médias complets :

-   Les sources multimédias doivent fournir des types de sortie complets.
-   Les décodeurs doivent fournir des types de sortie complets, une fois que le type d’entrée est défini. Avant de définir le type d’entrée, un décodeur peut fournir un type de sortie partiel.
-   Les encodeurs doivent fournir des types d’entrée complets, une fois le type de sortie défini. Avant de définir le type de sortie, un encodeur peut fournir un type d’entrée partiel.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de médias](media-types.md)
</dt> </dl>

 

 



