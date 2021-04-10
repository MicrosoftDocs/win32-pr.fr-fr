---
title: Volets de tâches du service
description: Volets de tâches du service
ms.assetid: f626fa85-7590-4e87-bd5c-7ffdcb14be8b
keywords:
- Magasins en ligne du lecteur Windows Media, volets des tâches du service
- magasins en ligne, volets des tâches de service
- types 2 magasins en ligne, volets de tâches de service
- Windows Media Player Online stores, volets des tâches
- magasins en ligne, volets des tâches
- tapez 2 magasins en ligne, volets des tâches
- Windows Media Player, service, volets Office
- Windows Media Player, volets des tâches
- volets de tâches du service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f882e46a7252792db5b551b25869c7711f9d31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029356"
---
# <a name="service-task-panes"></a>Volets de tâches du service

Dans le lecteur Windows Media 10, les fournisseurs de magasins en ligne peuvent configurer le lecteur Windows Media pour qu’ils affichent jusqu’à trois volets de tâches, appelés volets de tâches de service. Chaque volet de tâches de service est représenté par un bouton personnalisable que le lecteur Windows Media affiche sur le côté droit de la barre des tâches fonctionnalités.

Chaque volet de tâches de service héberge une page Web qui est l’interface utilisateur d’une fonctionnalité de magasin en ligne particulière. L’apparence des volets de tâches du service est définie par le document XML ServiceInfo. Dans ce document, les volets Office de service sont représentés par trois éléments : **ServiceTask1**, **ServiceTask2** et **ServiceTask3**. Ces volets de tâches de service sont conçus pour fournir les éléments suivants :

-   Un service musical.
-   Service vidéo.
-   Un service radio.

Vous pouvez positionner ces fonctionnalités dans le lecteur Windows Media dans n’importe quel ordre, mais **ServiceTask1** doit être le volet principal des tâches pour engager des activités commerciales.

La page Web hébergée dans chaque volet de tâches du service a accès à l’objet **externe** . Cet objet fournit des méthodes, des propriétés et un événement qui fournissent des fonctionnalités spéciales pour les pages Web dans le lecteur Windows Media. Par exemple, vous pouvez utiliser l’événement et les propriétés de **externe** pour que l’apparence de votre page Web corresponde au modèle de couleurs choisi par l’utilisateur pour le lecteur Windows Media.

Dans le lecteur Windows Media 11, il n’existe aucun volet Office de service. Au lieu de cela, il existe un onglet **magasins en ligne** unique, qui héberge la page Web principale du magasin en ligne actif. Dans le document ServiceInfo, l’onglet **magasins en ligne** est représenté par l’élément **ServiceTask1** ; les éléments **ServiceTask2** et **ServiceTask3** sont ignorés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des magasins en ligne de type 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Objet externe pour les magasins de type 2 en ligne**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**Document ServiceInfo pour un magasin de type 2 en ligne**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> </dl>

 

 




