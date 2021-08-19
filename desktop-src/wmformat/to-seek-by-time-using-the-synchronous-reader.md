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
ms.openlocfilehash: f74fb0cb4f73e70821347b82a9e5a2544eb9759e733fb164077b2fc007163db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118432632"
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

 

 




