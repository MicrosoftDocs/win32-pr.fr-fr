---
title: Volets de tâches du service
description: Volets de tâches du service
ms.assetid: f626fa85-7590-4e87-bd5c-7ffdcb14be8b
keywords:
- Lecteur Windows Media les magasins en ligne, volets des tâches de service
- magasins en ligne, volets des tâches de service
- types 2 magasins en ligne, volets de tâches de service
- Lecteur Windows Media des magasins en ligne, volets des tâches
- magasins en ligne, volets des tâches
- tapez 2 magasins en ligne, volets des tâches
- Lecteur Windows Media, volets des tâches de service
- Lecteur Windows Media, volets des tâches
- volets de tâches du service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d445e3fa5393dddb8e3dcc835317c8e5a284cb46f0a4a0e2b1f65fe2ea2d7b30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646509"
---
# <a name="service-task-panes"></a>Volets de tâches du service

dans Lecteur Windows Media 10, les fournisseurs de magasins en ligne peuvent configurer Lecteur Windows Media pour afficher jusqu’à trois volets de tâches, appelés volets de tâches de service. chaque volet de tâches de service est représenté par un bouton personnalisable qui Lecteur Windows Media s’affiche sur le côté droit de la barre des tâches fonctionnalités.

Chaque volet de tâches de service héberge une page Web qui est l’interface utilisateur d’une fonctionnalité de magasin en ligne particulière. L’apparence des volets de tâches du service est définie par le document XML ServiceInfo. Dans ce document, les volets Office de service sont représentés par trois éléments : **ServiceTask1**, **ServiceTask2** et **ServiceTask3**. Ces volets de tâches de service sont conçus pour fournir les éléments suivants :

-   Un service musical.
-   Service vidéo.
-   Un service radio.

vous pouvez positionner ces fonctionnalités dans Lecteur Windows Media dans n’importe quel ordre de votre choix, mais **ServiceTask1** doit être le volet principal des tâches pour engager des activités commerciales.

La page Web hébergée dans chaque volet de tâches du service a accès à l’objet **externe** . cet objet fournit des méthodes, des propriétés et un événement qui fournissent des fonctionnalités spéciales pour les pages web dans Lecteur Windows Media. par exemple, vous pouvez utiliser l’événement et les propriétés de **externe** pour que l’apparence de votre page web corresponde au modèle de couleurs choisi par l’utilisateur pour Lecteur Windows Media.

dans Lecteur Windows Media 11, il n’y a aucun volet de tâches de service. Au lieu de cela, il existe un onglet **magasins en ligne** unique, qui héberge la page Web principale du magasin en ligne actif. Dans le document ServiceInfo, l’onglet **magasins en ligne** est représenté par l’élément **ServiceTask1** ; les éléments **ServiceTask2** et **ServiceTask3** sont ignorés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des magasins en ligne de type 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Objet externe pour les magasins de type 2 en ligne**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**Document ServiceInfo pour un magasin de type 2 en ligne**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> </dl>

 

 




