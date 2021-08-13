---
description: les module de reconnaissance créés pour une utilisation avec Windows Vista et Windows XP édition Tablet PC utilisent un ensemble de structures, chacune d’elles étant appelée un treillis, pour repasser les résultats de la reconnaissance aux bibliothèques de plateformes Tablet pc.
ms.assetid: 628ca677-31eb-47d9-bcc6-d7777f8aaf7c
title: Structure de treillis de reconnaissance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5610d60428bd3259672f43e45efa59c25f78b7ddc5909c363610eaf08520e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716015"
---
# <a name="recognizer-lattice-structure"></a>Structure de treillis de reconnaissance

les module de reconnaissance créés pour une utilisation avec Windows Vista et Windows XP édition Tablet PC utilisent un ensemble de structures, chacune d’elles étant appelée un treillis, pour repasser les résultats de la reconnaissance aux bibliothèques de plateformes Tablet pc. La plateforme Tablet PC copie ensuite les informations de ces structures dans l’objet [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) , la collection [**IInkRecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) et l’objet [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) .

Un pointeur vers le treillis doit être retourné par le module de reconnaissance lorsque la plateforme appelle la fonction [**GetLatticePtr**](/windows/desktop/api/recapis/nf-recapis-getlatticeptr) sur le handle [HRECOCONTEXT](hrecocontext-handle.md) .

Cette section décrit en détail la structure de treillis. Pour obtenir une vue d’ensemble des identificateurs et des concepts associés, consultez à propos de la reconnaissance de l' [écriture manuscrite](about-handwriting-recognition.md).

## <a name="the-need-for-a-lattice"></a>Besoin d’un treillis

Un module de reconnaissance peut trouver plusieurs façons de rompre un ensemble de traits d’encre dans des segments de reconnaissance. Ce que le module de reconnaissance utilise comme segment de reconnaissance dépend du type de module de reconnaissance. Les module de reconnaissance de la langue anglaise utilisent généralement des mots comme segment de reconnaissance. D’autres reconnaissent peuvent utiliser des caractères, des formes ou des gestes comme segment de reconnaissance. La flexibilité des structures de treillis permet de gérer logiquement le grand nombre de résultats de la reconnaissance qui peuvent être combinés dans des relations complexes.

En interne, les détecteurs utilisent un treillis pour stocker les unités de reconnaissance de base pour une partie donnée de l’encre. Le treillis contient également le score, ou niveau de confiance, du résultat combiné. En outre, le treillis stocke le mappage des segments sur les traits d’encre d’origine.

Les structures de treillis sont définies dans le fichier d’en-tête rectypes. h. Les structures de treillis incluent les structures suivantes :

-   [**\_treillis é**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice)
-   [**\_colonne de treillis é \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column)
-   [**\_élément de treillis é \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)
-   [**\_Propriétés du treillis é \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_properties)
-   [**\_propriété de treillis é \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_property)

## <a name="lattice-components"></a>Composants de treillis

Les exemples suivants utilisent les traits pour le mot « ensemble », comme illustré dans l’image suivante. Dans les exemples, les segments sont évalués comme un ou plusieurs mots. Les nombres représentent les traits individuels dans le segment en cours d’évaluation. Notez que chacun des caractères « t » contient deux traits.

![traits pour le mot « ensemble »](images/1d5fa9fb-6c38-49b8-8caa-2b6dcc1d5dec.gif)

Un treillis est composé d’une ou plusieurs colonnes, une pour chaque segment. Chaque colonne contient à son tour un ou plusieurs éléments. Un élément contient une alternative de reconnaissance discrète. Pour plus d’informations sur les colonnes, consultez la structure de [**\_ \_ colonne de treillis é**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column) . Pour plus d’informations sur les éléments, consultez la structure de l' [**\_ \_ élément de treillis é**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element) .

Le module de reconnaissance peut retourner un segment unique lors de l’évaluation de l’exemple Ink indiqué dans l’exemple précédent. Dans ce cas, le treillis contient une seule colonne avec un seul élément.

Un exemple plus complexe se présente quand le module de reconnaissance évalue l’échantillon d’encre et s’affiche avec plusieurs segments et plusieurs alternatives pour chaque segment.

Le nombre de remplaçants de reconnaissance peut être échelonné, même pour un petit échantillon d’encre. Par exemple, « t o g e t h e r » peut générer les résultats suivants :

-   « pour l’obtenir » (plus de remplacements pour chaque mot)
-   « pour rassembler » (plus de remplacements pour chaque mot)
-   « pour obtenir son » (plus des alternatives pour chaque mot)
-   « ensemble » (plus des alternatives pour le mot)

Dans ce cas, un module de reconnaissance peut créer la structure de treillis suivante.

![structure de treillis pour le mot « ensemble »](images/2496c3dd-8b08-4f86-9fe3-f118be49a8c8.gif)

> [!Note]  
> Chaque colonne partage le même ordre des traits parce qu’ils font tous référence à la même collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .

 

 

 
