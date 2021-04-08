---
description: Pour obtenir un niveau de confiance pour chaque résultat de reconnaissance, vous pouvez obtenir la propriété Confidence de l’objet RecognitionAlternate ou la propriété Confidence de l’objet geste.
ms.assetid: b2495c5b-6db4-401c-ab7a-6556c55bbe46
title: Propriété confidence [à propos de la reconnaissance]
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f436d17d5cb83901c7d19ef4beb6dfb7ce6199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861917"
---
# <a name="confidence-property-about-recognition"></a>Propriété \[ de confiance sur la reconnaissance\]

Pour obtenir un niveau de confiance pour chaque résultat de reconnaissance, vous pouvez obtenir la propriété [**confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence) de l’objet [**RecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) ou la propriété [**confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence) de l’objet [**geste**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) . Le niveau de confiance est un nombre qui indique le degré de confiance de chaque autre résultat de reconnaissance que le module de reconnaissance renvoie pour un segment de reconnaissance correspondant.

La confiance est retournée comme faible, moyenne ou élevée. L’application utilise ces résultats pour :

-   Indiquez à l’utilisateur que plusieurs possibilités existent.
-   Classez les remplacements par niveau de confiance.

## <a name="what-affects-confidence"></a>Ce qui affecte la confiance

Certains éléments qui rendent la reconnaissance de l’écriture manuscrite difficile et affectent la confiance sont les suivants :

-   Difficulté à déterminer la segmentation des mots

![image indiquant une écriture trop proche](images/5c5d1c42-cbd1-46d0-a6f8-653f204f52cd.jpg)

-   Difficultés de cas

![image présentant des difficultés avec les versions manuscrites du mot « case »](images/1bdfb2e3-06ac-4c49-a39b-f0be51aed0e8.jpg)

-   Styles d’écriture rares
-   Ponctuation isolée

![image indiquant des guillemets trop éloignés du texte](images/743364b3-af62-4775-9d0d-f13f6e36c922.jpg)

-   Caractères accentués en anglais

> [!Note]  
> L’évaluation de la confiance est disponible uniquement pour États-Unis anglais et tous les module de reconnaissance de mouvement dans cette version. Les méthodes qui fournissent la propriété confidence pour tout autre module de reconnaissance retournent **E \_ NOTIMPL**.

 

 

 



