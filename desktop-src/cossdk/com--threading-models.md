---
description: Les modèles de thread COM+ sont conçus autour d’une collection d’objets appelée cloisonnement. Un cloisonnement est une collection de contextes contenus dans un processus.
ms.assetid: c73fb4c5-20ae-4873-afd2-4f40eb47bade
title: Modèles de thread COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f07b065861c042e68add633368a9c8b8ba41b2
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "103761114"
---
# <a name="com-threading-models"></a>Modèles de thread COM+

Les modèles de thread COM+ sont conçus autour d’une collection d’objets appelée cloisonnement. Un cloisonnement est une collection de contextes contenus dans un processus, comme indiqué dans l’illustration suivante.

![Diagramme qui montre une collection de contextes dans une activité, au sein d’un cloisonnement, au sein d’un processus.](images/6b86fe3b-262a-483a-a418-67d60f9a5d68.png)

Les appels au sein d’un cloisonnement sont directs, tandis que les appels entre les Apartments (out-of-process) sont indirects et requièrent du code proxy et stub. Les Apartments autorisent les objets avec des propriétés de synchronisation et de réentrance différentes et ont deux catégories : à thread unique et multithread. Les objets dans un thread cloisonné (STA) s’exécutent sur le thread particulier dans lequel ils ont été créés. Les STA autorisent l’exécution d’une seule méthode à la fois. Ils sont conçus pour les interfaces utilisateur et s’appuient sur la file d’attente de messages Microsoft Windows pour traiter les appels entrants.

Les objets d’un cloisonnement multithread (MTA) s’exécutent sur n’importe quel thread et permettent à un nombre quelconque de méthodes de se produire simultanément. Les MTA prennent en charge la réentrance implicitement.

Les classes COM+ sont marquées avec une propriété **ThreadingModel** qui permet à com+ de créer l’objet dans le cloisonnement approprié. Pour déterminer le cloisonnement dans lequel un objet est créé, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) utilise la propriété **ThreadingModel** .

Les threads doivent appeler [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) pour pouvoir utiliser com+. Cela les crée à l’intérieur du cloisonnement et du contexte appropriés. Le thread cloisonné principal est déterminé comme étant le premier STA appelé par **CoInitializeEx**. Cela est généralement associé au thread principal d’un processus. **CoInitializeEx** indique le type de cloisonnement requis par le thread en définissant les indicateurs suivants :

-   **COinit \_ MULTITHREAD**: localise le thread dans le seul cloisonnement multithread.
-   **COinit \_ APARTMENTTHREADED**: place le thread dans un nouveau STA.

Les rubriques suivantes de cette section fournissent des informations supplémentaires sur l’utilisation des modèles de thread et des cloisonnements dans COM+ :

-   [Attribut de modèle de thread](threading-model-attribute.md)
-   [Cloisonnements neutres](neutral-apartments.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Processus, threads et Apartments](/windows/desktop/com/processes--threads--and-apartments)
</dt> <dt>

[**ThreadingModel**](components.md)
</dt> </dl>

 

 
