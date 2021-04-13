---
title: Combinaison de l’architecture du gestionnaire de tables de routage
description: L’illustration suivante montre la relation entre les différents composants d’un routeur.
ms.assetid: 862566ce-47c4-424a-84c2-99f4c92efcc0
keywords:
- RTM, architecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc36c339ac89f01d5ba14c00857b3ced9c29414c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311593"
---
# <a name="how-the-routing-table-manager-architecture-fits-together"></a>Combinaison de l’architecture du gestionnaire de tables de routage

L’illustration suivante montre la relation entre les différents composants d’un routeur.

![relation entre les composants de routeur](images/rtsrvarch.png)

Lorsque le routeur est amorcé, le Service Router Manager est démarré, ainsi qu’un ou plusieurs protocoles de routage. Les protocoles de routage sont associés aux différentes interfaces sur le routeur. Le gestionnaire de routeur démarre également le gestionnaire de tables de routage.

L’illustration suivante montre la relation entre les clients et les différents composants du gestionnaire de tables de routage.

![relation entre les clients et les composants du gestionnaire de tables de routage](images/rtmentrel.png)

Le gestionnaire de routeur démarre une ou plusieurs instances du gestionnaire de tables de routage. Lorsque plusieurs instances du gestionnaire de tables de routage sont démarrées, le routeur a été configuré pour agir comme un ou plusieurs routeurs virtuels. Chaque instance du gestionnaire de tables de routage possède une ou plusieurs interfaces ; chaque interface ne peut appartenir qu’à une seule instance du gestionnaire de tables de routage.

Chaque instance du gestionnaire de tables de routage est indépendante des autres. aucune information n’est échangée entre les instances.

Chaque instance du gestionnaire de tables de routage contient une ou plusieurs tables de routage. Chaque table de routage est associée à une famille d’adresses.

Chaque table de routage contient une ou plusieurs vues. Dans cet exemple, la table de routage est affichée avec une vue monodiffusion et multidiffusion. Chaque vue est un sous-ensemble de la table de routage.

L’illustration suivante montre la relation entre les clients et plusieurs instances du gestionnaire de tables de routage, les tables de routage et les vues.

![clients de relation, gestionnaire de tables de routage, tables de routage, vues](images/multrtabrel.png)

Une instance du client peut s’inscrire plusieurs fois auprès d’une instance du gestionnaire de table de routage, une fois par famille d’adresses. Un client peut s’inscrire auprès de chaque instance du gestionnaire de tables de routage.

L’illustration suivante montre la relation entre les entrées de la table de routage. Pour plus d’informations sur les entrées de table de routage, consultez [entrées de table de routage](routing-table-entries.md).

![relation entre les entrées de la table de routage](images/nexthop.png)

La table de routage contient des destinations. Chaque destination est associée à un ou plusieurs itinéraires. Chaque itinéraire a zéro, un ou plusieurs pointeurs vers les tronçons suivants associés à l’itinéraire. Chaque pointeur fait référence au tronçon suivant réel dans la liste des tronçons suivants. Chaque client qui s’inscrit auprès du gestionnaire de tables de routage crée une liste de sauts suivants détenus par le client.

Les itinéraires ne peuvent contenir que des pointeurs vers la liste de tronçons suivants associée au client qui possède l’itinéraire.

 

 




