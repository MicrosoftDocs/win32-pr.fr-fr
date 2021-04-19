---
title: Capture directe à partir d’un appareil dans un fichier ASF (QASF)
description: Capture directe à partir d’un appareil dans un fichier ASF (QASF)
ms.assetid: 684a11e3-d507-4219-bc0b-6dfe5e85dad1
keywords:
- Windows Media Format SDK, capture à partir d’appareils dans des fichiers ASF (QASF)
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), capture à partir d’appareils (QASF)
- ASF (format avancé des systèmes), capture à partir d’appareils (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- DirectShow, capture à partir d’appareils dans des fichiers ASF (QASF)
- Windows Media Format SDK, QASF
- ASF (Advanced Systems Format), QASF
- ASF (format avancé des systèmes), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faaf5ba8df3cffbb2121451d3bd1b456fc994078
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106540752"
---
# <a name="capturing-directly-from-a-device-to-an-asf-file-qasf"></a>Capture directe à partir d’un appareil dans un fichier ASF (QASF)

Lorsque vous capturez du contenu audio ou vidéo directement dans un fichier ASF, le graphique de filtre ressemble à ce qui suit, selon le type de périphérique de capture utilisé.

![graphique de capture de l’image webcam vers WMV](images/asf-webcam.png)

La documentation du kit de développement logiciel (SDK) DirectShow décrit en détail comment créer des graphiques de capture, mais il y a un point important à retenir lors de la création de graphiques de capture à l’aide de l’enregistreur ASF de WM : l’enregistreur ASF WM ne s’exécute pas, sauf si tous ses codes confidentiels sont connectés. Si vous configurez l’enregistreur WM ASF avec le profil système par défaut (non recommandé), ou un profil avec des flux audio et vidéo, il créera une broche d’entrée pour chaque flux et chacune de ces broches doit être connectée. Si vous n’envisagez pas de capturer de l’audio, par exemple, assurez-vous de configurer le filtre avec un profil vidéo uniquement afin qu’aucun code confidentiel audio ne soit créé.

 

 




