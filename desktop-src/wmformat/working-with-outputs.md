---
title: Utilisation des sorties
description: Utilisation des sorties
ms.assetid: e2e14e88-dddc-496d-8087-1455da0821e3
keywords:
- Windows Media Format SDK, utilisation des sorties
- ASF (Advanced Systems Format), utilisation des sorties
- ASF (format avancé des systèmes), utilisation des sorties
- ASF (Advanced Systems Format), nombres et formats de sortie
- ASF (format des systèmes avancés), nombres et formats de sortie
- nombres et formats de sortie, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274e5b4980ef14126006d3f19fe0717aa9eb6fd5c1a8f7baaf91e35084faeacb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697723"
---
# <a name="working-with-outputs"></a>Utilisation des sorties

Par défaut, chaque exemple que vous recevez de l’un des deux objets de lecteur est associé à un numéro de sortie. Chaque numéro de sortie correspond à un flux du fichier ASF. Le lecteur attribue des numéros de sortie aux flux du fichier lorsque le fichier est ouvert. Normalement, il y a une sortie pour chaque flux dans un fichier. Toutefois, si le fichier utilise l’exclusion mutuelle, un seul numéro de sortie est attribué à chaque groupe de flux mutuellement exclusifs. Le flux qui correspond au numéro de sortie des flux s’excluant mutuellement est déterminé par le lecteur, dans le cas de fichiers à débit binaire multiple (MBR) ou par votre application, si vous utilisez la sélection manuelle de flux.

Étant donné que le nom de connexion défini dans le profil n’est pas conservé dans le fichier, le lecteur crée un nom de connexion par défaut pour chaque sortie qui est simplement une représentation sous forme de chaîne du numéro de sortie, par exemple « 1 », « 2 », « 3 », etc. Les noms de connexion permettent aux applications et au lecteur lui-même de mettre en corrélation les sorties avec les flux. Dans un fichier à plusieurs vitesses de transmission, plusieurs flux partagent un nom de connexion. Cela n’a pas d’importance pour le lecteur, car les propriétés de sortie de chaque flux MBR sont identiques.

Chaque sortie a un ou plusieurs formats de sortie pris en charge. Un format de sortie est le format que les exemples non compressés fournis par le lecteur utilisent. Lorsque le lecteur ouvre un fichier, il définit le format de chaque sortie sur la valeur par défaut pour le sous-type de média. Le nombre et le type des formats de sortie pris en charge sont déterminés par le codec qui décompresse les données multimédias.

Les rubriques suivantes expliquent comment utiliser les sorties :

-   [Pour identifier les numéros de sortie](to-identify-output-numbers.md)
-   [Assigner des formats de sortie](assigning-output-formats.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Interface IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lecture des fichiers ASF**](reading-asf-files.md)
</dt> </dl>

 

 




