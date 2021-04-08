---
description: Les contrôles de média et d’appel TAPI 3 sont un ensemble générique d’objets COM, d’interfaces et de méthodes permettant d’effectuer des appels entre deux machines ou plus.
ms.assetid: e345df2f-1b68-41be-ac2d-b771136ee831
title: À propos des contrôles Call et Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65d1a10d004cb16e0ba8753c27665cb7a30ff3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869565"
---
# <a name="about-call-and-media-controls"></a>À propos des contrôles Call et Media

Les contrôles de média et d’appel TAPI 3 sont un ensemble générique d’objets COM, d’interfaces et de méthodes permettant d’effectuer des appels entre deux machines ou plus. Dans le contexte de l’interface TAPI 3, l' *appel* fait référence non seulement à la transmission vocale sur le réseau public commuté (RTPC), mais aussi aux moyens et moyens de transport pour lesquels des fournisseurs de services existent : par exemple, une conférence multimédia multidiffusion s’exécutant sur un intranet d’entreprise.

Les cinq objets principaux dans l’architecture d’appel et de contrôle de média TAPI 3 sont [TAPI](tapi-object.md), [Address](address-object.md), [Terminal](terminal-object.md), [Call](call-object.md)et [CallHub](callhub-object.md). En outre, des mises en service ont été apportées pour les [interfaces spécifiques au fournisseur](provider-specific-interfaces.md).

Le diagramme suivant illustre la façon dont ces objets interagissent.

![interactions entre les objets TAPI 3,0 Call et les objets MCI](images/sdkobj2.png)

## <a name="features"></a>Fonctionnalités

-   Fait abstraction des fonctionnalités d’appel et de support pour permettre aux protocoles de communication différents et apparemment incompatibles d’exposer une interface commune aux applications.
-   Basé sur le modèle COM (Component Object Model), les applications peuvent être écrites dans pratiquement n’importe quel langage. Si vous avez besoin d’informations supplémentaires sur COM, consultez le kit de développement logiciel (SDK) de la plateforme.
-   Contrôle d’appel fourni par les fournisseurs de services de téléphonie (TSPs), qui implémentent des mécanismes spécifiques au transport.
-   Contrôle multimédia fourni par les fournisseurs de services de média (MSP). Les MSP actuels utilisent DirectShow. DirectShow est un système modulaire de composants enfichables appelés filtres, organisés dans une configuration appelée graphique de filtre. Le gestionnaire de graphique de filtre supervise la connexion de ces filtres et contrôle le flux de données du flux. Si vous avez besoin d’informations supplémentaires sur DirectShow, consultez le kit de développement logiciel (SDK) de la plateforme.

 

 



