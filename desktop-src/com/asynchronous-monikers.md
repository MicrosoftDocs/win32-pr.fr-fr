---
title: Monikers asynchrones
description: Monikers asynchrones
ms.assetid: 24c50f7b-f085-4086-aa44-81e5cab011cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19323af3a972a2b83a290176a4b26fb79382da0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106509881"
---
# <a name="asynchronous-monikers"></a>Monikers asynchrones

L’architecture du moniker OLE fournit un modèle de programmation cohérent et extensible pour travailler avec des objets Internet, en fournissant des méthodes pour l’analyse des noms, en représentant des localisateurs de ressources universelles (URL) comme noms imprimables et en localisant les objets représentés par des chaînes d’URL et en les liant. (Voir également [monikers d’URL](url-monikers.md).) Toutefois, les monikers OLE standard (notamment les monikers d’élément, de fichier et de pointeur) ne sont pas appropriés pour Internet, car ils sont synchrones et retournent un pointeur vers un objet ou son stockage uniquement à un moment où toutes les données sont disponibles. Selon la quantité de données à télécharger, la liaison synchrone peut bloquer l’interface utilisateur du client pendant des périodes prolongées.

Internet requiert de nouvelles approches pour la conception d’applications. Les applications doivent être en mesure d’effectuer toutes les opérations réseau coûteuses de manière asynchrone afin d’éviter de bloquer l’interface utilisateur. Une application doit être en mesure de déclencher une opération et de recevoir une notification en cas de saisie semi-automatique complète ou partielle. À ce stade, l’application doit être en mesure de passer à l’étape suivante de l’opération ou de fournir des informations supplémentaires en fonction des besoins. Au cours du téléchargement, une application doit également être en mesure de fournir aux utilisateurs des informations sur la progression et la possibilité d’annuler l’opération à tout moment.

Les monikers asynchrones fournissent ces fonctionnalités, ainsi que divers niveaux de comportement de liaison asynchrone, tout en fournissant une compatibilité descendante pour les applications qui ignorent ou ne nécessitent pas de comportement asynchrone. Une autre technologie OLE, stockage asynchrone, fonctionne avec les monikers asynchrones pour assurer le téléchargement asynchrone de l’état persistant d’un objet Internet. Le moniker asynchrone déclenche l’opération de liaison et configure les composants nécessaires, y compris le stockage et les objets de flux, les objets de tableau d’octets et les récepteurs de notification. Une fois les composants connectés, le moniker est hors de la voie et le reste de la liaison est exécuté principalement entre les composants qui implémentent les composants de stockage asynchrones et l’objet.

Pour plus d'informations, voir les rubriques suivantes :

-   [Monikers asynchrones et synchrones](./asynchronous-vs.-synchronous-monikers.md)
-   [Liaison asynchrone et synchrone](./asynchronous-vs.-synchronous-binding.md)
-   [Stockage asynchrone et synchrone](./asynchronous-vs.-synchronous-storage.md)
-   [Modèle d’extraction de données et modèle de Data-Push](./data-pull-model-vs.-data-push-model.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Monikers d’URL](url-monikers.md)
</dt> </dl>

 

 