---
title: Image Flux
description: Image Flux
ms.assetid: 17a945aa-463a-4aac-82cc-68b49c720c0a
keywords:
- Windows Media Format SDK, images flux
- ASF (Advanced Systems Format), flux d’images
- ASF (format des systèmes avancés), flux d’images
- Windows Media Format SDK, Streams
- ASF (Advanced Systems Format), flux
- ASF (format de systèmes avancés), flux
- flux d’images, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2067710e6b2be627bd16125d73e567a2f1ba1557ae01b81f55712d8c5a7b8bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702863"
---
# <a name="image-streams"></a>Image Flux

Un flux d’image est un type spécial de flux qui contient des images fixes affectées aux durées de présentation. Une application peut afficher les images dans un flux d’image comme vous le souhaitez, mais l’implémentation classique consiste à afficher chaque image jusqu’à ce que l’image suivante soit remise, comme un diaporama. En règle générale, un flux d’image est encodé dans un fichier avec un flux audio pour produire une présentation simple d’images synchronisées avec de la musique ou de la parole.

Les flux d’images sont semblables aux flux vidéo dans la mesure où ils sont créés à partir d’exemples non compressés qui sont compressés dans le cadre du processus d’écriture de fichier, mais ils sont également des flux arbitraires, car vous devez affecter une vitesse de transmission et une fenêtre de mémoire tampon appropriées au contenu sans utiliser les propriétés affectées par un codec.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Flux arbitraire**](arbitrary-streams.md)
</dt> <dt>

[**Fonctionnalités des fichiers ASF**](asf-file-features.md)
</dt> <dt>

[**Flux audio et vidéo**](audio-and-video-streams.md)
</dt> <dt>

[**Écriture d’une image Flux**](writing-image-streams.md)
</dt> </dl>

 

 




