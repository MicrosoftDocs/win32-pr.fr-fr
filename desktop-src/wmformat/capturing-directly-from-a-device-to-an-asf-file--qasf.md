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
ms.openlocfilehash: 570e773e39b4c2d76bd95f0a4ac90269be295585ef91e6e50f653b121cbc8d9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705087"
---
# <a name="capturing-directly-from-a-device-to-an-asf-file-qasf"></a>Capture directe à partir d’un appareil dans un fichier ASF (QASF)

Lorsque vous capturez du contenu audio ou vidéo directement dans un fichier ASF, le graphique de filtre ressemble à ce qui suit, selon le type de périphérique de capture utilisé.

![graphique de capture de l’image webcam vers WMV](images/asf-webcam.png)

la documentation du kit de développement logiciel (SDK) DirectShow décrit en détail comment créer des graphiques de capture, mais il y a un point important à retenir lors de la création de graphiques de capture à l’aide de l’enregistreur asf de wm : l’enregistreur asf wm ne s’exécute pas, sauf si tous ses codes confidentiels sont connectés. Si vous configurez l’enregistreur WM ASF avec le profil système par défaut (non recommandé), ou un profil avec des flux audio et vidéo, il créera une broche d’entrée pour chaque flux et chacune de ces broches doit être connectée. Si vous n’envisagez pas de capturer de l’audio, par exemple, assurez-vous de configurer le filtre avec un profil vidéo uniquement afin qu’aucun code confidentiel audio ne soit créé.

 

 




