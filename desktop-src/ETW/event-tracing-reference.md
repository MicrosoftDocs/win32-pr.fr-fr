---
description: Répertorie les éléments utilisés avec le suivi d’événements.
ms.assetid: 8cb5907e-9006-45d1-9d48-13a43a631664
title: Référence de suivi d’événements
ms.topic: article
ms.date: 01/30/2020
ms.openlocfilehash: 7e0ee4576b9b9d64a5766c6ab096ea34abc2b176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973659"
---
# <a name="event-tracing-reference"></a>Référence de suivi d’événements

Vous utilisez les éléments de programmation suivants pour écrire des applications qui intègrent le suivi d’événements :

-   [Énumérations de suivi d’événements](/windows/desktop/api/_etw/#enumerations)
-   [Fonctions de suivi d’événements](/windows/desktop/api/_etw/#functions)
-   [Interfaces de suivi d’événements](/windows/desktop/api/_etw/#interfaces)
-   [Structures de suivi d’événements](/windows/desktop/api/_etw/#structures)
-   [Constantes de suivi d’événements](event-tracing-constants.md)

Pour plus d’informations sur les exemples qui utilisent ces éléments de programmation, consultez [exemples de traçage d’événements](event-tracing-samples.md).

Cette section contient également des informations sur les éléments suivants :

-   [Outils](event-tracing-tools.md) fournis par ETW
-   [Définitions de classe MOF](event-tracing-mof-classes.md) pour les événements de noyau
-   [Qualificateurs de classe MOF](event-tracing-mof-qualifiers.md) utilisés lors de la définition de vos classes d’événements

## <a name="process-etw-traces-in-net-code"></a>Traiter les traces ETW dans le code .NET

Vous pouvez également utiliser l' [API .net TraceProcessing](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) pour analyser les traces ETW pour vos applications et d’autres composants logiciels. Cette API est utilisée en interne chez Microsoft pour analyser les données ETW produites par le système d’ingénierie Windows, et elle est également utilisée pour alimenter plusieurs tables dans l' [Analyseur de performances Windows](/windows-hardware/test/wpt/windows-performance-analyzer). Cette API est disponible sous la forme d’un package NuGet.

Pour plus d’informations, consultez [cet article](/windows/apps/trace-processing/overview).
