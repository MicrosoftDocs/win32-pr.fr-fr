---
title: À propos des services Web Windows
description: L’API des services Web Windows est une API en couches et peut être illustrée comme suit.
ms.assetid: 6e8c23d1-c86b-432d-8e0c-e16982849239
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7546aaa72d58e43d7faefccf394a3e27756f4a96
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104568695"
---
# <a name="about-windows-web-services"></a>À propos des services Web Windows

L’API des services Web Windows est une API en couches et peut être illustrée comme suit

![Diagramme montrant les couches et les zones inter-couches de l’API des services Web Windows.](images/apistack.png)

Le WWSAPI est une API en couches. Nous pensons que la plupart des développeurs ciblent le modèle de service, qui est un modèle de programmation basé sur une méthode. Dans le modèle de service, l’hôte de service fournit le modèle de programmation côté serveur, tandis que le proxy de service fournit le modèle de programmation côté client.

Chaque couche expose un ensemble d’API et de types qui peuvent être utilisés avec les API de cette couche.

## <a name="service-model"></a>Modèle de service

La couche de niveau supérieur appelée le [modèle de service](service-model-layer-overview.md) fournit un modèle de programmation basé sur une méthode qui est le modèle le plus simple à utiliser. Dans le modèle de service, l' [hôte de service](service-host.md) fournit le modèle de programmation côté serveur, tandis que le proxy de [service](service-proxy.md) fournit le modèle de programmation côté client. Le [contexte](context.md) est utilisé dans le modèle de service pour passer un État pertinent à la disposition de l’opération de service et/ou du rappel lorsqu’il est appelé. Le [contrat de service](contract.md) est utilisé pour spécifier un contrat de service sur un point de terminaison exposé sur le service. Les composants et opérations suivants font partie de la couche de service :

-   [Hôte de service](service-host.md)
-   [Proxy de service](service-proxy.md)
-   [Contexte](context.md)
-   [Façon](contract.md)
-   [Métadonnées du service](service-metadata.md)

## <a name="channel-layer"></a>Couche de canal

Le modèle de service repose sur une couche de canal, ce qui offre une flexibilité totale, mais est plus difficile à utiliser. Les composants et opérations suivants font partie de la couche de canal :

-   [Message](message.md)
-   [Channel](channel.md)
-   [Port d'écoute](listener.md)
-   [Erreurs](faults.md)
-   [Url](url.md)
-   [Sécurité](security-overview.md)
-   [Importation de métadonnées](metadata-import.md)

## <a name="xml-layer"></a>Couche XML

La couche de canal est à son tour basée sur une infrastructure XML légère, qui comprend la désérialisation des types de données C. Les composants et opérations suivants font partie de la couche XML :

-   [Enregistreur XML](xml-writer.md)
-   [Lecteur XML](xml-reader.md)
-   [Mémoire tampon XML](xml-buffer.md)
-   [Sérialisation](serialization.md)
-   [Prise en charge du langage XML](xml-language-support.md)

## <a name="common-to-all-layers"></a>Commun à toutes les couches

Les rubriques suivantes s’appliquent à l’une des trois couches :

-   [Erreurs](errors.md)
-   [Modèle asynchrone](asynchronous-model.md)
-   [Cohérence de thread](thread-safety.md)
-   [Suivi](tracing.md)
-   [Annulation](cancellation.md)
-   [Utilitaires](utilities.md)
-   [Débogage](debugging.md)
-   [Outil compilateur Wsutil](wsutil-compiler-tool.md)
-   [Système](heap.md)

## <a name="examples"></a>Exemples

Pour plus d’informations sur les éléments d’API, consultez [référence des services Web Windows](windows-web-services-reference.md). Pour obtenir des exemples d’utilisation de l’API, consultez [utilisation des services Web Windows](using-windows-web-services.md).

 

 




