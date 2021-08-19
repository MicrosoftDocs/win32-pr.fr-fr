---
description: Présentation de DirectShow
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: Présentation de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51cd4dc2a75233c519c4ca3d5db213451b097c0528ab782109da611b6e35aca7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952578"
---
# <a name="introduction-to-directshow"></a>Présentation de DirectShow

microsoft® DirectShow® est une architecture de diffusion multimédia en continu sur la plateforme Microsoft Windows®. DirectShow offre une capture et une lecture de grande qualité des flux multimédias. Il prend en charge une grande variété de formats, notamment les fichiers ASF (Advanced Systems Format), MPEG (motion image experts Group), AVI (Audio-Video entrelacé), MPEG Audio Layer-3 (MP3) et les fichiers audio WAV. il prend en charge la capture à partir d’appareils numériques et analogiques basés sur le Windows Driver Model (WDM) ou vidéo pour Windows. Il détecte et utilise automatiquement le matériel d’accélération vidéo et audio lorsqu’il est disponible, mais il prend également en charge les systèmes sans accélération matérielle.

DirectShow est basé sur le modèle COM (component Object Model). pour écrire une application ou un composant DirectShow, vous devez comprendre la programmation du client COM. Pour la plupart des applications, il n’est pas nécessaire d’implémenter vos propres objets COM. DirectShow fournit les composants dont vous avez besoin. toutefois, si vous souhaitez étendre DirectShow en écrivant vos propres composants, vous devez les implémenter en tant qu’objets COM.

DirectShow est conçu pour C++. Microsoft ne fournit pas d’API gérée pour DirectShow.

DirectShow simplifie la lecture du média, la conversion de format et les tâches de capture. En même temps, il fournit l’accès à l’architecture du contrôle de flux sous-jacent pour les applications qui nécessitent des solutions personnalisées. vous pouvez également créer vos propres composants de DirectShow pour prendre en charge de nouveaux formats ou des effets personnalisés.

voici quelques exemples de types d’applications que vous pouvez écrire avec DirectShow inclure les lecteurs de fichiers, les lecteurs TV et DVD, les applications de montage vidéo, les convertisseurs de format de fichier, les applications de capture audio-video, les encodeurs et les décodeurs, les processeurs de signal numérique, etc.

Cette section contient les rubriques suivantes :

-   [Nouveautés de DirectShow](whats-new-in-directshow.md)
-   [Formats pris en charge dans DirectShow](supported-formats-in-directshow.md)
-   [DirectShow FAQ](directshow-faq.yml)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main](getting-started.md)
</dt> <dt>

[Utilisation de DirectShow](using-directshow.md)
</dt> </dl>

 

 



