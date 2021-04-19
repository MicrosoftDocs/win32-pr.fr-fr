---
title: États des objets
description: États des objets
ms.assetid: 8ebef6d6-7a2f-4b95-91ca-999646cde82d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 268b9bc9c69009850a5172259ab7a13c760d2c72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511206"
---
# <a name="object-states"></a>États des objets

Un objet composé existe dans l’un des trois États suivants : passif, chargé ou en cours d’exécution. L’état d’un objet de document composé décrit la relation entre l’objet dans son conteneur et l’application responsable de sa création. Le tableau suivant récapitule ces États.



| État de l’objet       | Description                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Passif<br/> | L’objet composé-document existe uniquement dans le stockage, soit sur le disque soit dans une base de données. Dans cet État, l’objet n’est pas disponible pour l’affichage ou la modification.<br/>                                                                                                                                                                                                                                   |
| Loaded<br/>  | Les structures de données de l’objet créées par le gestionnaire d’objets se trouvent dans la mémoire du conteneur. Le conteneur a établi la communication avec le gestionnaire d’objets et des données de présentation mises en cache sont disponibles pour le rendu de l’objet. Les appels sont traités par le gestionnaire d’objets. Cet État, en raison de sa faible surcharge, est utilisé lorsqu’un utilisateur affiche ou imprime simplement un objet.<br/> |
| En cours d’exécution<br/> | Les objets qui contrôlent la communication à distance ont été créés et l’application serveur OLE est en cours d’exécution. Les interfaces de l’objet sont accessibles et le conteneur peut recevoir la notification des modifications. Dans cet État, un utilisateur final peut modifier ou manipuler l’objet.<br/>                                                                                                                    |



 

Pour plus d'informations, voir les rubriques suivantes :

-   [Passage à l’État chargé](entering-the-loaded-state.md)
-   [Passage à l’État en cours d’exécution](entering-the-running-state.md)
-   [Passage à l’état passif](entering-the-passive-state.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Documents composés](compound-documents.md)
</dt> </dl>

 

 





