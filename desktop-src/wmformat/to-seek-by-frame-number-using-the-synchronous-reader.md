---
title: Pour rechercher par numéro de frame à l’aide du lecteur synchrone
description: Pour rechercher par numéro de frame à l’aide du lecteur synchrone
ms.assetid: 755e0124-de57-4699-af8e-c594567b5523
keywords:
- ASF (Advanced Systems Format), recherche par numéro de trame
- ASF (format avancé des systèmes), recherche par numéro de trame
- ASF (Advanced Systems Format), lecteurs synchrones
- ASF (format des systèmes avancés), lecteurs synchrones
- lecteurs synchrones, recherche par numéros de frame
- flux vidéo, recherche par numéros de frame
- flux vidéo, lecteurs synchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e1b2da615f23e5c1d17046f08310d0aeda49200d5c4ba9fba890d7ba4951e0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699110"
---
# <a name="to-seek-by-frame-number-using-the-synchronous-reader"></a>Pour rechercher par numéro de frame à l’aide du lecteur synchrone

Pour rechercher des données par numéro de trame à l’aide du lecteur synchrone, vous spécifiez une plage pour la lecture. Une plage est définie par un numéro de frame de début dans un flux vidéo spécifique et un nombre de frames à lire.

Pour rechercher des données dans un fichier ASF par numéro de trame à l’aide du lecteur synchrone, procédez comme suit.

1.  Définissez le nombre de frames de départ et le nombre d’images à lire pour l’exemple de remise en appelant [**IWMSyncReader :: SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe). Vous devez spécifier le numéro de flux d’un flux vidéo indexé par une image. Le lecteur synchronise le reste des sorties avec l’heure de présentation du frame spécifié du flux spécifié et commence à fournir des exemples de sortie.
2.  Commencez la récupération des exemples avec des appels à [**IWMSyncReader :: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Procédez comme vous le feriez normalement avec le lecteur synchrone.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lecture des fichiers avec le lecteur synchrone**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




