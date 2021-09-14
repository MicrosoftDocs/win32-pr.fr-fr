---
description: Choisissez une classe de base dans le cadre de l’écriture d’un filtre de transformation. Découvrez les classes appropriées pour les filtres de transformation.
ms.assetid: 4b2d3add-0430-480b-ad5f-bb1aa19fef21
title: Étape 1. Choisir une classe de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1a2bbf704bb2247034bc2ba3a6f35812f46aaaa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240653"
---
# <a name="step-1-choose-a-base-class"></a>Étape 1. Choisir une classe de base

Il s’agit de l’étape 1 du didacticiel [écriture de filtres de transformation](writing-transform-filters.md).

en supposant que vous décidiez d’écrire un filtre et non un DMO, la première étape consiste à choisir la classe de base à utiliser. Les classes suivantes sont appropriées pour les filtres de transformation :

-   [**CTransformFilter**](ctransformfilter.md) est conçu pour les filtres de transformation qui utilisent des mémoires tampons d’entrée et de sortie distinctes. Ce type de filtre est parfois appelé filtre de transformation de copie. Lorsqu’un filtre de transformation de copie reçoit un exemple d’entrée, il écrit de nouvelles données dans un exemple de sortie et remet l’exemple de sortie au filtre suivant.
-   [**CTransInPlaceFilter**](ctransinplacefilter.md) est conçu pour les filtres qui modifient les données dans la mémoire tampon d’origine, également appelées filtres de transfert sur place. Lorsqu’un filtre TRANS-in-place reçoit un échantillon, il modifie les données de cet exemple et remet le même échantillon en aval. La broche d’entrée et la broche de sortie du filtre se connectent toujours aux types de médias correspondants.
-   [**CVideoTransformFilter**](cvideotransformfilter.md) est principalement conçu pour les décodeurs vidéo. Il dérive de **CTransformFilter**, mais il comprend des fonctionnalités permettant de supprimer des frames si le convertisseur en aval se trouve en arrière-plan.
-   [**CBaseFilter**](cbasefilter.md) est une classe de filtre générique. Les autres classes de cette liste dérivent toutes de **CBaseFilter**. Si aucun de ces éléments ne convient, vous pouvez revenir sur cette classe. Toutefois, cette classe nécessite également le plus de travail de votre part.
-   \[! Précieuse\]  
    > Les transformations vidéo sur place peuvent avoir un impact sérieux sur les performances de rendu. Les transformations sur place nécessitent des opérations de lecture-modification-écriture sur la mémoire tampon. Si la mémoire réside sur une carte graphique, les opérations de lecture sont beaucoup plus lentes. En outre, même une transformation de copie peut entraîner des opérations de lecture involontaires si vous ne l’implémentez pas avec prudence. Par conséquent, vous devez toujours effectuer des tests de performances si vous écrivez une transformation vidéo.

     

Pour l’exemple d’encodeur RLE, le meilleur choix est **CTransformFilter** ou **CVideoTransformFilter**. En fait, les différences entre elles sont en grande partie internes. il est donc facile de les convertir de l’une à l’autre. Étant donné que les types de médias doivent être différents sur les deux codes confidentiels, la classe **CTransInPlaceFilter** n’est pas appropriée pour ce filtre. Cet exemple utilise **CTransformFilter**.

Suivant : [étape 2. Déclarez la classe de filtre](step-2--declare-the-filter-class.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[écriture de filtres de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



