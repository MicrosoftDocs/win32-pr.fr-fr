---
description: Paramètres de média
ms.assetid: 48b2bc2e-897d-4aa9-8a50-c2855a17dca5
title: Paramètres de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9276a3d38b9176458299bfd1a47057cac6236e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869473"
---
# <a name="media-parameters"></a>Paramètres de média

Les paramètres de média permettent à une application de configurer les propriétés d’un objet afin qu’elles évoluent dans le temps d’une manière mathématique déterministe.

Par exemple, supposons qu’un ingénieur de son mélange une bande maître numérique et souhaite appliquer un léger délai à une section de voix pour remplir le son. L’effet sera transférerez si le retard se découpe brusquement. Au lieu de cela, l’effet doit commencer à 100 pour cent (sans délai) et la combinaison humide/sèche doit augmenter graduellement jusqu’à atteindre le niveau souhaité. En outre, cette transition doit suivre une courbe lisse ou une progression linéaire. Pour prendre en charge ce scénario, un DMO peut exposer les interfaces suivantes :

-   [**IMediaParamInfo**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) contient des méthodes permettant de découvrir des informations sur les propriétés prises en charge. En règle générale, le client appellera ces méthodes avant de commencer à diffuser des données en continu.
-   [**IMediaParams**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) contient des méthodes permettant de définir les courbes qu’un paramètre suivra pendant la diffusion en continu.

Ces interfaces sont principalement conçues pour DMOs, mais tout objet peut les prendre en charge. Dans cette section, le terme *paramètre* fait référence à toute propriété qui prend en charge ces deux interfaces.

Cette section contient les rubriques suivantes :

-   [Courbes de paramètres](parameter-curves.md)
-   [Informations sur les paramètres](parameter-information.md)
-   [Segments d’enveloppe](envelope-segments.md)
-   [Calcul des valeurs de paramètre](calculating-parameter-values.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets multimédia DirectX](directx-media-objects.md)
</dt> </dl>

 

 



