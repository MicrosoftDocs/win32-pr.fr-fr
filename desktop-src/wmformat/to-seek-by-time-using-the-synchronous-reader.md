---
title: Pour effectuer une recherche par heure à l’aide du lecteur synchrone
description: Pour effectuer une recherche par heure à l’aide du lecteur synchrone
ms.assetid: 143f72b0-9d71-4efa-b8d4-5cde53a2aa2a
keywords:
- ASF (Advanced Systems Format), recherche par heure
- ASF (format de systèmes avancés), recherche par heure
- ASF (Advanced Systems Format), lecteurs synchrones
- ASF (format des systèmes avancés), lecteurs synchrones
- lecteurs synchrones, recherche par heure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a43e914a6fc0d320860db61f4747cbee3033e9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723562"
---
# <a name="to-seek-by-time-using-the-synchronous-reader"></a>Pour effectuer une recherche par heure à l’aide du lecteur synchrone

Pour rechercher des données à l’aide du lecteur synchrone, vous spécifiez une plage pour la lecture. Une plage est définie par une heure de début de présentation et une durée, à la fois en unités de 100 nanosecondes.

Pour rechercher des données dans un fichier ASF par heure de présentation à l’aide du lecteur synchrone, procédez comme suit.

1.  Spécifiez une heure de début et une durée pour l’exemple de remise en appelant [**IWMSyncReader :: SetRange**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange). Cette méthode ne vous oblige pas à spécifier un numéro de flux, car les durées de présentation de chaque flux doivent déjà être synchronisées.
2.  Commencez la récupération des exemples avec des appels à [**IWMSyncReader :: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Procédez comme vous le feriez normalement avec le lecteur synchrone.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lecture des fichiers avec le lecteur synchrone**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




