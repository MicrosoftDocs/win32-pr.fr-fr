---
title: Transcodage de fichiers (QASF)
description: Transcodage de fichiers (QASF)
ms.assetid: c6dad6cf-4781-4204-883b-cdb33aff5e27
keywords:
- Windows Media Format SDK, transcodage des fichiers (QASF)
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), fichiers de transcodage (QASF)
- ASF (format des systèmes avancés), fichiers de transcodage (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- DirectShow, fichiers de transcodage (QASF)
- Windows Media Format SDK, QASF
- ASF (Advanced Systems Format), QASF
- ASF (format avancé des systèmes), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7465c98edd39d173623f202dfdf7845dfeda648c52106f2241ea596d54caa00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929162"
---
# <a name="transcoding-files-qasf"></a>Transcodage de fichiers (QASF)

Vous pouvez créer un graphique de filtre de transcodage de fichiers à l’aide du [writer WM ASF](wm-asf-writer-filter.md) de différentes façons. Le moyen le plus simple consiste à co-créer, à configurer et à ajouter l’enregistreur ASF WM au graphique de filtre, puis à utiliser la méthode **IGraphBuilder :: RenderFile** pour générer le graphique automatiquement.

Une autre méthode consiste à ajouter manuellement chaque filtre au graphique et à connecter les broches. Après avoir ajouté l’enregistreur ASF WM, configurez-le à l’aide des méthodes **IConfigAsfWriter** si le profil par défaut n’est pas approprié et connectez les broches d’entrée du writer ASF pour les broches de sortie correspondantes sur les filtres en amont.

L’illustration suivante montre les configurations typiques du graphique de filtre de transcodage WM ASF Writer.

![diagrammes de filtre de transcodage standard](images/asf-transcode.png)

 

 




