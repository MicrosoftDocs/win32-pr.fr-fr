---
title: Liaison dynamique
description: Les développeurs de graphiques créent parfois des nuanceurs de grande taille et à usage général qui peuvent être utilisés par un large éventail d’éléments de scène.
ms.assetid: 2f5f7852-0f0a-4fad-a412-9a0d634c73b6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d5cd10bab8e2b4a28458cad1050847e0184ce43b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673441"
---
# <a name="dynamic-linking"></a>Liaison dynamique

Les développeurs de graphiques créent parfois des nuanceurs de grande taille et à usage général qui peuvent être utilisés par un large éventail d’éléments de scène. Lors de l’exécution, le nuanceur exécute de manière conditionnelle le code approprié pour la situation donnée. Malheureusement, ces gros nuanceurs à usage général utilisent des registres à usage général (GPRs) de manière inefficace et peuvent être beaucoup plus lents que les plus petits et les plus petits.

Le Shader Model 5 résout ce problème de performances en introduisant une liaison de nuanceur dynamique. La liaison dynamique sépare les fragments de code du nuanceur en utilisant des interfaces et des fonctions virtuelles et permet à l’application de sélectionner le fragment à utiliser au moment du tracé. Cela améliore les performances en liant uniquement le code du nuanceur nécessaire et non l’intégralité du nuanceur à usage général.

## <a name="in-this-section"></a>Dans cette section



| Élément                                                                                                                                                                                                                                                                                                                         | Description                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="Storing_Variables_and_Types_for_Shaders_to_Share"></span><span id="storing_variables_and_types_for_shaders_to_share"></span><span id="STORING_VARIABLES_AND_TYPES_FOR_SHADERS_TO_SHARE"></span>[Stockage des variables et des types pour les nuanceurs à partager](storing-variables-and-types-for-shaders-to-share.md)<br/> | Décrit l’objet de liaison de classe pour stocker des variables et des types que plusieurs nuanceurs peuvent partager.<br/> |
| <span id="Interfaces_and_Classes"></span><span id="interfaces_and_classes"></span><span id="INTERFACES_AND_CLASSES"></span>[Interfaces et classes](overviews-direct3d-11-hlsl-dynamic-linking-class.md)<br/>                                                                                                         | Décrit l’utilisation d’interfaces et de classes HLSL pour implémenter la liaison dynamique.<br/>                           |
| <span id="Interface_Usage_Restrictions"></span><span id="interface_usage_restrictions"></span><span id="INTERFACE_USAGE_RESTRICTIONS"></span>[Restrictions d’utilisation de l’interface](overviews-direct3d-11-hlsl-dynamic-linking-expression.md)<br/>                                                                            | Décrit les restrictions sur l’utilisation des interfaces dans le code du nuanceur.<br/>                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[HLSL](overviews-direct3d-11-hlsl.md)
</dt> </dl>

 

 





