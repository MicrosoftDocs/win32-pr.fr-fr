---
description: Pourquoi l’encodeur vidéo rejette-t-il un format de sortie que j’essaie de définir, lorsque j’ai récupéré le format du même objet ?
ms.assetid: f0747450-d224-423a-a9f1-04580df8a17e
title: Pourquoi l’encodeur vidéo rejette-t-il un format de sortie que j’essaie de définir, lorsque j’ai récupéré le format du même objet ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680908ec814fe322585c1ac97d3bb79deddaf034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034289"
---
# <a name="why-does-the-video-encoder-reject-an-output-format-that-i-try-to-set-when-i-retrieved-the-format-from-the-same-object"></a>Pourquoi l’encodeur vidéo rejette-t-il un format de sortie que j’essaie de définir, lorsque j’ai récupéré le format du même objet ?

Contrairement aux types de sortie de l’encodeur audio, les sorties prises en charge énumérées par les encodeurs vidéo ne sont pas complètes comme remises. Vous devez définir la vitesse de transmission du flux dans le membre **dwBitrate** de la structure **VIDEOINFOHEADER** pour qu’elle corresponde à la valeur définie pour la propriété [ \_ RAVG MFPKEY](mfpkey-ravgproperty.md) .

Une fois toutes les options définies comme vous le souhaitez, vous devez récupérer les données privées du codec et les ajouter à la structure **VIDEOINFOHEADER** . Pour plus d’informations, consultez [utilisation de données privées de codec vidéo](usingvideocodecprivatedata.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Questions fréquentes (FAQ)](frequentlyaskedquestions.md)
</dt> </dl>

 

 



