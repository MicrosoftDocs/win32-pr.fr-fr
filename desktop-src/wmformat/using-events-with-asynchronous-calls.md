---
title: Utilisation d’événements avec des appels asynchrones
description: Utilisation d’événements avec des appels asynchrones
ms.assetid: 98c24176-a632-400e-b23b-5e13f1bd9a27
keywords:
- Windows Media Format SDK, événements avec appels asynchrones
- Windows Media Format SDK, appels asynchrones (événements)
- événements, appels asynchrones
- événements d’appel asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1729108cae5b73ec96be208709c1360e9401ac0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380268"
---
# <a name="using-events-with-asynchronous-calls"></a>Utilisation d’événements avec des appels asynchrones

Souvent, lorsque vous utilisez des méthodes qui sont appelées de façon asynchrone, vous devez arrêter le traitement de votre application jusqu’à ce que la méthode termine le traitement. Vous pouvez implémenter n’importe quelle technique pour gérer cette situation. Cette section décrit l’utilisation d’un événement pour attendre des appels asynchrones dans le thread appelant. Cette technique est fréquemment utilisée avec le kit de développement logiciel (SDK) du format Windows Media et est illustrée dans certains des exemples d’applications.

La liste suivante résume l’utilisation des événements pour attendre des appels asynchrones.

1.  Créez un événement à utiliser avec votre application en appelant la fonction **CreateEvent** du kit de développement logiciel (SDK) de plateforme.
2.  Lorsque vous implémentez les rappels appropriés pour votre application, interceptez les messages que vous devez attendre. Dans la logique de gestion des messages pour les messages souhaités, signalez l’événement en appelant la fonction **SetEvent** du kit de développement logiciel (SDK) de plateforme.
3.  Une fois les appels aux événements asynchrones effectués dans votre application, attendez que l’événement signale en appelant la fonction **WaitForSingleObject** du kit de développement logiciel (SDK) de la plateforme. Si vous concevez une application Windows, vous devez créer une boucle pour rechercher les messages Windows et inclure un appel à **WaitForSingleObject** dans la boucle avec un délai d’attente bref.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des méthodes de rappel**](using-the-callback-methods.md)
</dt> </dl>

 

 




