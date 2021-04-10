---
title: Pour accéder aux statistiques de performances des lecteurs
description: Pour accéder aux statistiques de performances des lecteurs
ms.assetid: 996abfe6-1444-48ab-8c34-ba923c4cd511
keywords:
- ASF (Advanced Systems Format), statistiques de performances des lecteurs
- ASF (format des systèmes avancés), statistiques des performances du lecteur
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), statistiques de performances
- ASF (format de systèmes avancés), statistiques de performances
- lecteurs asynchrones, statistiques de performances
- performances, statistiques sur les lecteurs
- performances, lecteurs asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5484b211f2c2d1e9ad4cf9aac3773c7946757c2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841889"
---
# <a name="to-get-reader-performance-statistics"></a>Pour accéder aux statistiques de performances des lecteurs

Lors de la lecture de fichiers localement avec le lecteur asynchrone, il n’est pas nécessaire de vérifier les performances des opérations de lecture. Toutefois, si votre application lit à partir d’une source de streaming, les statistiques de performances peuvent être très importantes. Votre application peut répondre aux modifications des performances de lecture pour garantir la meilleure expérience possible pour l’utilisateur final.

Les informations de performances que vous pouvez récupérer à partir du lecteur incluent les statistiques suivantes :

-   Bande passante actuelle de la connexion.
-   Nombre de paquets reçus à partir du serveur.
-   Nombre de paquets perdus qui ont été récupérés.
-   Nombre de paquets perdus qui n’ont pas été récupérés.
-   Pourcentage du nombre total de paquets envoyés qui ont été reçus.

Pour accéder aux statistiques de performances des lecteurs, procédez comme suit.

1.  Avant de commencer la lecture, créez une structure de [**\_ \_ statistiques WM Reader**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) . Vous devez définir le membre **cbSize** sur sizeof ( \_ statistiques du lecteur WM \_ ).
2.  Obtenez un pointeur vers l’interface [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) de l’objet lecteur en appelant **IWMReader :: QueryInterface**.
3.  Pendant la lecture, effectuez fréquemment des appels à [**IWMReaderAdvanced :: GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) pour surveiller les performances. Transmettez votre structure de **\_ \_ statistiques de lecteur WM** avec chaque appel et examinez les membres appropriés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecture des fichiers avec le lecteur asynchrone**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




