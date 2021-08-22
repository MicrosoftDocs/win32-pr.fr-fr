---
description: Configuration du décodage vidéo
ms.assetid: 897b8e2d-9827-428d-91ae-632038c4c8c0
title: Configuration du décodage vidéo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7c49d42b47b4b6745731287e2b0bf0ee2d21c1eb503ed561274a5fb4cc8b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035337"
---
# <a name="configuring-video-decoding-microsoft-media-foundation"></a>Configuration du décodage vidéo (Microsoft Media Foundation)

Le décodage est essentiellement l’opposé de l’encodage en termes de configuration. Le décodeur prend en charge très peu de propriétés et aucun d’entre eux n’est requis. Définissez le type d’entrée sur le type utilisé pour la sortie du décodeur (y compris les données privées du codec). Ensuite, définissez la sortie au format non compressé souhaité, définissez la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) pour qu’elle reflète la taille d’image appropriée et commencez le traitement des exemples.

Vous devez fournir au décodeur un type de média qui comprend les données privées de codec positionnées immédiatement après la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . Le décodeur ne peut pas décoder le contenu sans ces données. La validation de format effectuée par le décodeur ne valide pas les données privées. Si les données privées du codec sont manquantes ou incorrectes, le décodeur répond comme si le flux de bits était endommagé. Pour plus d’informations, consultez [utilisation de données privées de codec vidéo](usingvideocodecprivatedata.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de données privées de codec vidéo](usingvideocodecprivatedata.md)
</dt> <dt>

[Utilisation de la vidéo](workingwithvideo.md)
</dt> </dl>

 

 
