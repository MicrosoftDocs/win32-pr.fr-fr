---
title: Windows Référence du journal des événements
description: Voici les éléments de programmation que vous utilisez pour créer un manifeste d’instrumentation, créer des ressources à partir du manifeste utilisé par votre fournisseur, obtenir les métadonnées d’instrumentation au moment de l’exécution et interroger les événements à partir des canaux et des fichiers journaux
ms.assetid: 7af07a43-62f6-412f-9f67-46ad08922daf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6ce52f3756b8f33ac710e189677de053dc538339d0a0cdeb335410dd76a171
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957789"
---
# <a name="windows-event-log-reference"></a>Windows Référence du journal des événements

Voici les éléments de programmation que vous utilisez pour créer un manifeste d’instrumentation, créer des ressources à partir du manifeste utilisé par votre fournisseur, obtenir les métadonnées d’instrumentation au moment de l’exécution et interroger des événements à partir des canaux et des fichiers journaux :

-   [Schéma EventManifest](eventmanifestschema-schema.md)
-   [Schéma d’événement](eventschema-schema.md)
-   [Schéma de requête](queryschema-schema.md)
-   [Windows Constantes du journal des événements](windows-event-log-constants.md)
-   [Windows Types de données du journal des événements](windows-event-log-data-types.md)
-   [Windows Énumérations des journaux des événements](windows-event-log-enumerations.md)
-   [Windows Fonctions du journal des événements](windows-event-log-functions.md)
-   [Windows Structures du journal des événements](windows-event-log-structures.md)
-   [Windows Outils du journal des événements](windows-event-log-tools.md)

pour les applications écrites à l’aide d’un langage .net, telles que C# ou Visual Basic, consultez les espaces de noms suivants :

-   Pour écrire des événements, utilisez les classes et méthodes définies dans l’espace de noms [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) .
-   pour consommer des événements à partir d’un canal Windows journal des événements ou d’un journal, utilisez les classes et méthodes définies dans l’espace de noms [System. diagnostics. eventing. Reader](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) .

Comme alternative à l’utilisation de l’espace de noms [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) pour écrire des événements, vous pouvez utiliser l’argument **-CS** ou **-CSS** pour que le compilateur de message génère le code pour écrire les événements. Pour plus d’informations, consultez [**message compiler**](message-compiler--mc-exe-.md).
