---
description: Type de format VideoInfo2
ms.assetid: edd2013a-f0c5-4176-ba3a-a3af719ce31d
title: Type de format VideoInfo2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b0f435e0e2a1b5b1d948c42a881f19300a9c6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527781"
---
# <a name="videoinfo2-format-type"></a>Type de format VideoInfo2

Le type de média préféré d’un pin d’aperçu peut être un type avec un format [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . Cette structure de format prend en charge des fonctionnalités spéciales telles que les proportions de vidéo et d’image entrelacées.

VMR-7 et VMR-9 prennent en charge [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) directement. Quand vous connectez VMR au décodeur, il négocie le meilleur format. Toutefois, le filtre de convertisseur vidéo plus ancien ne prend pas en charge **VIDEOINFOHEADER2**. Pour utiliser les types de format **VIDEOINFOHEADER2** avec le filtre de convertisseur vidéo, vous devez insérer le filtre de [mixage de superposition](overlay-mixer-filter.md) dans le graphique.

1.  Énumérez les types de médias préférés sur la broche de sortie du filtre de décodeur, à l’aide de la méthode [**IPIN :: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .
2.  Vérifiez le premier type de média dans la séquence d’énumération.
3.  Si le type de format **est \_ VideoInfo2 format**, connectez la broche de sortie au mélangeur de superposition. Connectez ensuite le mixer de superposition au convertisseur vidéo. (Voir les [broches des ports vidéo](video-port-pins.md).)

Si vous ne vous souciez pas de ces fonctionnalités, vous n’avez pas besoin d’utiliser le mélangeur de superposition. Connectez le décodeur directement au convertisseur vidéo et il se connectera avec un format [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) à la place.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rubriques avancées sur la capture](advanced-capture-topics.md)
</dt> <dt>

[Utilisation du mélangeur de superposition dans la capture vidéo](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



