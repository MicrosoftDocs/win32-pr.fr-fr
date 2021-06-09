---
description: Présentation de DirectShow
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: Présentation de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5706ff0dec34c5db3762f5782f96804e5c85e889
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827223"
---
# <a name="introduction-to-directshow"></a>Présentation de DirectShow

Microsoft® DirectShow® est une architecture de diffusion multimédia en continu sur la plateforme Microsoft Windows®. DirectShow offre une capture et une lecture de grande qualité des flux multimédias. Il prend en charge une grande variété de formats, notamment les fichiers ASF (Advanced Systems Format), MPEG (motion image experts Group), AVI (Audio-Video entrelacé), MPEG Audio Layer-3 (MP3) et les fichiers audio WAV. Il prend en charge la capture à partir d’appareils numériques et analogiques basés sur le Windows Driver Model (WDM) ou vidéo pour Windows. Il détecte et utilise automatiquement le matériel d’accélération vidéo et audio lorsqu’il est disponible, mais il prend également en charge les systèmes sans accélération matérielle.

DirectShow est basé sur le modèle COM (Component Object Model). Pour écrire une application ou un composant DirectShow, vous devez comprendre la programmation du client COM. Pour la plupart des applications, il n’est pas nécessaire d’implémenter vos propres objets COM. DirectShow fournit les composants dont vous avez besoin. Toutefois, si vous souhaitez étendre DirectShow en écrivant vos propres composants, vous devez les implémenter en tant qu’objets COM.

DirectShow est conçu pour C++. Microsoft ne fournit pas d’API gérée pour DirectShow.

DirectShow simplifie la lecture du média, la conversion de format et les tâches de capture. En même temps, il fournit l’accès à l’architecture du contrôle de flux sous-jacent pour les applications qui nécessitent des solutions personnalisées. Vous pouvez également créer vos propres composants DirectShow pour prendre en charge de nouveaux formats ou des effets personnalisés.

Parmi les types d’applications que vous pouvez écrire avec DirectShow, citons les lecteurs de fichiers, les lecteurs TV et DVD, les applications de modification vidéo, les convertisseurs de format de fichier, les applications de capture audio-video, les encodeurs et les décodeurs, les processeurs de signal numérique, et bien plus encore.

Cette section contient les rubriques suivantes :

-   [Nouveautés de DirectShow](whats-new-in-directshow.md)
-   [Formats pris en charge dans DirectShow](supported-formats-in-directshow.md)
-   [FAQ DirectShow](directshow-faq.yml)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main](getting-started.md)
</dt> <dt>

[Utilisation de DirectShow](using-directshow.md)
</dt> </dl>

 

 



