---
title: lecture Flux avec des Pixels Non carrés
description: lecture Flux avec des Pixels Non carrés
ms.assetid: 32114c81-cb78-43de-9ea7-f210056f5aab
keywords:
- Windows Media Format SDK, lire les flux vidéo
- Windows Media Format SDK, flux vidéo
- Windows Media Format SDK, pixels non carrés
- Windows Media Format SDK, pixels (non carré)
- ASF (Advanced Systems Format), lecture des flux vidéo
- ASF (format des systèmes avancés), lire les flux vidéo
- ASF (Advanced Systems Format), flux vidéo
- ASF (format de systèmes avancés), flux vidéo
- ASF (Advanced Systems Format), pixels non carrés
- ASF (format des systèmes avancés), pixels non carrés
- Format de systèmes avancés (ASF), pixels (non carrés)
- ASF (format des systèmes avancés), pixels (non carrés)
- lecture des flux vidéo
- flux vidéo, lecture
- flux vidéo, pixels non carrés
- pixels non carrés
- pixels (non carrés)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfc14019e9822aefedb7600adc4209317293b2f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404646"
---
# <a name="reading-streams-with-non-square-pixels"></a>lecture Flux avec des Pixels Non carrés

Les applications de lecteur qui doivent gérer correctement les pixels non carrés doivent examiner à la fois les attributs au niveau du flux dans l’en-tête ASF et les extensions d’unité de données sur chaque exemple. Il existe deux cas où le rectangle de sortie doit être ajusté pour compenser les pixels non carrés.

Lorsque le contenu source a été capturé à partir d’un appareil tel qu’une caméra DV (vidéo numérique) avec des pixels non carrés dans son CCD, une application de lecteur doit ajuster son rectangle de sortie vidéo afin que l’image s’affiche correctement sur un moniteur d’ordinateur avec des pixels carrés.

Lorsque votre application de lecteur produit une vidéo qui est lue sur une télévision NTSC, par exemple par le biais d’une connexion out S-Video sur la carte vidéo, vous devez ajuster le rectangle vidéo afin que l’image s’affiche correctement sur les pixels non carrés de la télévision.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**pour lire et écrire des Flux vidéo avec des Pixels Non carrés**](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




