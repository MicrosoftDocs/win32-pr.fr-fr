---
description: Un effet Microsoft DirectX permet d’intégrer des nuanceurs vertex et de pixels à l’état du pipeline pour afficher des objets. Les effets sont l’étape logique suivante dans la combinaison de nuanceurs pour produire des conditions de rendu uniques.
ms.assetid: vs|directx_sdk|~\effects.htm
title: Effets (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59ed52a3a75f4b0682be4447f02ed305cf026af6aa30a59e921f4fa23f0e2211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985983"
---
# <a name="effects-direct3d-9"></a>Effets (Direct3D 9)

Un effet Microsoft DirectX permet d’intégrer des nuanceurs vertex et de pixels à l’état du pipeline pour afficher des objets. Les effets sont l’étape logique suivante dans la combinaison de nuanceurs pour produire des conditions de rendu uniques.

Les effets offrent également un moyen pratique d’écrire des nuanceurs pour différentes versions matérielles. Étant donné que différentes cartes vidéo prennent en charge des fonctionnalités différentes, une application peut écrire plusieurs techniques qui s’exécuteront sur divers appareils. De cette façon, si l’application s’exécute sur le matériel le plus récent et le plus grand, l’application peut exécuter la technique d’effet la plus sophistiquée. En revanche, les techniques d’effet moins complexes peuvent être automatiquement choisies pour s’exécuter sur du matériel moins onéreux ou moins performant.

Un effet peut remplacer le traitement du vertex et une partie du traitement des pixels effectué par le pipeline Graphics. Un exemple d’effet qui utilise un nuanceur de sommets et un nuanceur de pixels se trouve dans l’exemple BasicHLSL. Vous pouvez obtenir cet exemple et en savoir plus à ce sujet à partir du kit de développement logiciel (SDK) DirectX. Pour plus d’informations sur DirectX SDK, consultez [où se trouve le kit de développement logiciel (SDK) DirectX ?](../directx-sdk--august-2009-.md).

Pour plus d’informations sur les effets, consultez les rubriques suivantes :

-   [Écriture d’un effet](writing-an-effect.md)
-   [Utilisation d’un effet](using-an-effect.md)

## <a name="effects-and-the-3d-pipeline"></a>Effets et le pipeline 3D

Le diagramme suivant illustre le pipeline.

![diagramme du pipeline 3D](images/effects-block-diagram.png)

Le pipeline transforme les données d’entrée en pixels de sortie qui remplissent la mémoire tampon de trame. Les données d’entrée proviennent d’objets composés de sommets dans l’espace d’objet, ou de surfaces d’ordre supérieur créées à partir des N-patchs, des carreaux de rectangles et des carreaux de triangle. Une fois que les données d’entrée ont été fractionnées, le pipeline effectue le traitement des vertex, le traitement de la primitive et le traitement des pixels avant de générer les couleurs finales des pixels.

Le traitement des vertex et des pixels peut être effectué par le pipeline de fonction fixe ou peut être implémenté avec des nuanceurs programmables. Le pavage des données d’entrée, le traitement de la primitive et les sorties de données sont contrôlés par l’état du pipeline. Tout cela peut être intégré à un effet. Un effet définit l’État qui contrôle le mode de fonctionnement du pipeline. Les effets gèrent les nuanceurs programmables ainsi que l’état de fonction fixe.

Les effets peuvent enregistrer et restaurer l’État, laissant l’appareil dans le même État qu’avant l’exécution de l’effet. Les types d’État qu’un effet peut gérer sont les suivants :

-   État du nuanceur. Cela comprend la création et la suppression des nuanceurs, la définition des constantes de nuanceur, la définition de l’état du nuanceur et le rendu avec des nuanceurs.
-   État de la texture et de l’échantillonneur. Cela comprend la spécification de fichiers de texture, l’initialisation des étapes de texture, la création d’objets d’échantillonnage et la définition de l’état de l’échantillonneur.
-   Autre État du pipeline. Cela comprend les États pour définir les transformations, l’éclairage, les matériaux et les options de rendu. Il peut s’agir de variables globales ou locales. Les variables peuvent être définies par l’effet lui-même ou par l’application.

Les effets contiennent plusieurs options de rendu appelées techniques. Chaque technique encapsule les variables globales, l’état du pipeline, l’état de la texture et de l’échantillonneur, ainsi que l’état du nuanceur. Un style unique est implémenté dans une passe de rendu. Une ou plusieurs passes peuvent être encapsulées dans une technique. Toutes les passes et toutes les techniques peuvent être validées pour voir si le code d’effet s’exécutera sur le périphérique matériel.

## <a name="effects-save-and-restore-state"></a>État de l’enregistrement et de la restauration des effets

État de la gestion des effets. L’état du mot est largement utilisé ici, car il comprend tous les types d’informations dont le pipeline a besoin pour spécifier les conditions de rendu. Cela comprend presque toutes les zones fonctionnelles du pipeline.

Les options de rendu sont contrôlées par des techniques et des passes. Une application restitue un effet en définissant une technique active et en affichant une ou plusieurs passes. Tout rendu dans un effet est effectué dans une paire correspondante d’appels [**Begin**](id3dxeffect--begin.md) et [**end**](id3dxeffect--end.md) . Lorsque **Begin** est appelé, un stateblock est créé et l’état de l’appareil est enregistré (sauf indication contraire). Une fois qu’une technique a rendu les passes que l’application spécifie de rendre, **end** est appelé pour mettre fin à la technique active. Le système d’effet répond en restaurant automatiquement l’état du pipeline qui a été capturé dans le bloc d’État (sauf si vous choisissez de désactiver cette fonctionnalité d’enregistrement et de restauration).

Lors de la programmation de séquences de rendu à plusieurs étapes, chacune nécessitant sa propre configuration d’État, les effets peuvent réduire la maintenance requise pour le suivi des modifications d’État. Pour obtenir plus d’informations sur les États qui peuvent être enregistrés et restaurés par les effets, consultez [États d’effet (Direct3D 9)](effect-states.md).

## <a name="effects-can-share-parameters"></a>Les effets peuvent partager des paramètres

Les paramètres Effects sont toutes les variables non statiques déclarées dans un effet. Cela peut inclure des variables globales et des annotations. Les paramètres Effects peuvent être partagés entre différents effets en déclarant des paramètres avec le mot clé Shared, puis en créant l’effet avec un pool Effect.

Les effets clonés utilisent le même pool d’effets que l’effet à partir duquel ils sont clonés. Le clonage d’un effet fait une copie exacte d’un effet, y compris les variables globales, les techniques, les passes et les annotations.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour Direct3D 9](dx9-graphics-programming-guide.md)
</dt> </dl>

 

 
