---
description: Implémentez la prise en charge de la négociation de type de média dans le cadre de l’écriture d’un filtre de transformation. Le type de média décrit le format des données.
ms.assetid: b2b5dafc-d38d-4ec3-a390-55229495b4f9
title: Étape 3. Prendre en charge la négociation de type de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a23784e70330f751325fc5f780463d5a3904d20
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410042"
---
# <a name="step-3-support-media-type-negotiation"></a>Étape 3. Prendre en charge la négociation de type de média

Il s’agit de l’étape 3 du didacticiel [écriture de filtres de transformation](writing-transform-filters.md).

Lorsque deux codes confidentiels se connectent, ils doivent s’accorder sur un type de support pour la connexion. Le type de média décrit le format des données. Sans le type de média, un filtre peut fournir un type de données, uniquement pour qu’un autre filtre le traite comme autre chose.

Le mécanisme de base pour la négociation des types de média est la méthode [**IPIN :: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) . La broche de sortie appelle cette méthode sur la broche d’entrée avec un type de média proposé. La broche d’entrée accepte la connexion ou la rejette. Si la connexion est rejetée, la broche de sortie peut essayer un autre type de média. Si aucun type approprié n’est trouvé, la connexion échoue. Si vous le souhaitez, la broche d’entrée peut publier une liste de types qu’elle préfère, par le biais de la méthode [**IPIN :: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) . La broche de sortie peut utiliser cette liste lorsqu’elle propose des types de média, bien qu’elle ne soit pas nécessaire.

La classe **CTransformFilter** implémente un Framework général pour ce processus, comme suit :

-   La broche d’entrée n’a pas de type de média préféré. Il s’appuie entièrement sur le filtre amont pour proposer le type de média. Pour les données vidéo, cela est logique, car le type de média comprend la taille de l’image et la fréquence d’images. En règle générale, ces informations doivent être fournies par un filtre de source en amont ou un filtre d’analyseur. Dans le cas de données audio, l’ensemble de formats possibles est plus petit, donc il peut être pratique que la broche d’entrée offre des types préférés. Dans ce cas, remplacez [**CBasePin :: GetMediaType**](cbasepin-getmediatype.md) sur la broche d’entrée.
-   Quand le filtre amont propose un type de média, la broche d’entrée appelle la méthode [**CTransformFilter :: CheckInputType**](ctransformfilter-checkinputtype.md) , qui accepte ou rejette le type.
-   La broche de sortie ne se connecte pas, sauf si la broche d’entrée est connectée en premier. Ce comportement est courant pour les filtres de transformation. Dans la plupart des cas, le filtre doit déterminer le type d’entrée avant de pouvoir définir le type de sortie.
-   Lorsque la broche de sortie se connecte, elle dispose d’une liste de types de médias qu’elle propose au filtre en aval. Elle appelle la méthode [**CTransformFilter :: GetMediaType**](ctransformfilter-getmediatype.md) pour générer cette liste. La broche de sortie essaiera également tous les types de supports que le filtre en aval propose.
-   Pour vérifier si un type de sortie particulier est compatible avec le type d’entrée, la broche de sortie appelle la méthode [**CTransformFilter :: CheckTransform**](ctransformfilter-checktransform.md) .

Les trois méthodes **CTransformFilter** répertoriées ci-dessus sont des méthodes virtuelles pures, donc votre classe dérivée doit les implémenter. Aucune de ces méthodes n’appartient à une interface COM ; ils font simplement partie de l’implémentation fournie par les classes de base.

Les sections suivantes décrivent chaque méthode plus en détail :

-   [Étape 3A. Implémenter la méthode CheckInputType](step-3a--implement-the-checkinputtype-method.md)
-   [Étape 3B. Implémenter la méthode GetMediaType](step-3b--implement-the-getmediatype-method.md)
-   [Étape 3C. Implémenter la méthode CheckTransform](step-3c--implement-the-checktransform-method.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Connexion des filtres](how-filters-connect.md)
</dt> <dt>

[Écriture de filtres DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



