---
title: Informations de référence sur le journal des événements Windows
description: Voici les éléments de programmation que vous utilisez pour créer un manifeste d’instrumentation, créer des ressources à partir du manifeste utilisé par votre fournisseur, obtenir les métadonnées d’instrumentation au moment de l’exécution et interroger les événements à partir des canaux et des fichiers journaux
ms.assetid: 7af07a43-62f6-412f-9f67-46ad08922daf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fef1af82cdab1ab92b4ea4768479541053fe65d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033617"
---
# <a name="windows-event-log-reference"></a>Informations de référence sur le journal des événements Windows

Voici les éléments de programmation que vous utilisez pour créer un manifeste d’instrumentation, créer des ressources à partir du manifeste utilisé par votre fournisseur, obtenir les métadonnées d’instrumentation au moment de l’exécution et interroger des événements à partir des canaux et des fichiers journaux :

-   [Schéma EventManifest](eventmanifestschema-schema.md)
-   [Schéma d’événement](eventschema-schema.md)
-   [Schéma de requête](queryschema-schema.md)
-   [Constantes du journal des événements Windows](windows-event-log-constants.md)
-   [Types de données du journal des événements Windows](windows-event-log-data-types.md)
-   [Énumérations des journaux des événements Windows](windows-event-log-enumerations.md)
-   [Fonctions du journal des événements Windows](windows-event-log-functions.md)
-   [Structures du journal des événements Windows](windows-event-log-structures.md)
-   [Outils du journal des événements Windows](windows-event-log-tools.md)

Pour les applications écrites à l’aide d’un langage .NET, telles que C# ou Visual Basic, consultez les espaces de noms suivants :

-   Pour écrire des événements, utilisez les classes et méthodes définies dans l’espace de noms [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) .
-   Pour consommer des événements à partir d’un canal ou d’un journal des événements Windows, utilisez les classes et méthodes définies dans l’espace de noms [System. Diagnostics. Eventing. Reader](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) .

Comme alternative à l’utilisation de l’espace de noms [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) pour écrire des événements, vous pouvez utiliser l’argument **-CS** ou **-CSS** pour que le compilateur de message génère le code pour écrire les événements. Pour plus d’informations, consultez [**message compiler**](message-compiler--mc-exe-.md).
