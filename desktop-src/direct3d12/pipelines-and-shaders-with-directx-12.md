---
title: Pipelines et nuanceurs avec Direct3D 12
description: Le pipeline programmable Direct3D 12 augmente considérablement les performances de rendu par rapport aux interfaces de programmation graphique de génération précédente.
ms.assetid: 329882F5-D2A9-4D6D-AC3B-29F370D22C97
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2c392b3915443da2f287a5511f3959cbb7179f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104548527"
---
# <a name="pipelines-and-shaders-with-direct3d-12"></a>Pipelines et nuanceurs avec Direct3D 12

Le pipeline programmable Direct3D 12 augmente considérablement les performances de rendu par rapport aux interfaces de programmation graphique de génération précédente.

-   [Pipeline graphique Direct3D 12](#direct3d-12-graphics-pipeline)
-   [Objets d’état de pipeline](#pipeline-state-objects)
-   [Pipeline de calcul Direct3D 12](#direct3d-12-compute-pipeline)
-   [Rubriques connexes](#related-topics)

## <a name="direct3d-12-graphics-pipeline"></a>Pipeline graphique Direct3D 12

Le diagramme suivant illustre l’État et le pipeline de graphiques Direct3D 12.

![Diagramme illustrant l’État et le pipeline Direct3D 12](images/pipeline.png)

Un pipeline Graphics est le workflow séquentiel des entrées et sorties de données à mesure que le GPU restitue des frames. Étant donné l’état du pipeline et les entrées, le GPU effectue une série d’opérations pour créer les images résultantes. Un pipeline graphique contient des nuanceurs qui effectuent des calculs et des effets de rendu programmables, ainsi que des opérations de fonction fixes.

Notez les points suivants lorsque vous faites référence au diagramme d’État du pipeline :

-   Les tables de descripteurs et les tas peuvent être disposés arbitrairement : SRVs, CBVs et UAVs peuvent être référencés et alloués dans n’importe quel ordre.
-   Certaines opérations du pipeline sont configurables. Par exemple, la fusion de sortie fonctionne généralement sur une base de lecture-modification-écriture avec les vues de la cible de rendu et du stencil de profondeur. Toutefois, le pipeline peut être configuré de sorte que l’un de ces affichages soit en lecture seule ou en écriture seule.
-   Les échantillonneurs statiques ne font pas partie des arguments racine, car ils sont statiques.

## <a name="pipeline-state-objects"></a>Objets d’état de pipeline

Direct3D 12 introduit l’objet d’État du pipeline (PSO). Au lieu de stocker et de représenter l’état du pipeline sur un grand nombre d’objets de niveau supérieur, les États des composants de pipeline tels que l’assembleur d’entrée, le rastériseur, le nuanceur de pixels et la fusion de sortie sont stockés dans un objet PSO. Un objet PSO est un objet d’état de pipeline unifié qui est immuable après la création. L’PSO actuellement sélectionné peut être modifié rapidement et de façon dynamique, et le matériel et les pilotes peuvent convertir directement un PSO en instructions et États matériels natifs, en préservant le GPU pour le traitement des graphiques. Pour appliquer un PSO, le matériel copie une quantité minimale d’État précalculé directement dans les registres matériels. Cela supprime la surcharge causée par le pilote Graphics qui recalcule continuellement l’état du matériel en fonction de tous les paramètres de pipeline et de rendu actuellement applicables. Le résultat est considérablement réduit la surcharge des appels de dessin, des performances accrues et d’autres appels de dessin par trame.

L’PSO actuellement appliqué définit et connecte tous les nuanceurs utilisés dans le pipeline de rendu. Le [langage HLSL (High Level Shader Language) de Microsoft](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) est précompilé en objets nuanceur, qui sont ensuite utilisés au moment de l’exécution en tant qu’entrée pour les objets d’état de pipeline. Pour plus d’informations sur le fonctionnement des fonctions PSO dans le pipeline Graphics, consultez [gestion de l’état des pipelines graphiques dans Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

## <a name="direct3d-12-compute-pipeline"></a>Pipeline de calcul Direct3D 12

Le diagramme suivant illustre l’État et le pipeline de calcul Direct3D 12.

![Diagramme qui montre le pipeline de calcul Direct3D 12.](images/compute-pipeline.png)

Il n’y a pas d’unités de fonction fixe dans ce pipeline, mais les tas de descripteurs, les tas d’échantillonneur et les échantillonneurs statiques sont toujours disponibles dans Compute.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Envoi de travail dans Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

 