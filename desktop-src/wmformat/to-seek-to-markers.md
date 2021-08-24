---
title: Pour rechercher des marqueurs
description: Pour rechercher des marqueurs
ms.assetid: 2d5efebf-dcbd-4fb8-933e-cc6d3a99adf8
keywords:
- ASF (Advanced Systems Format), recherche de marqueurs
- ASF (format de systèmes avancés), recherche de marqueurs
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), marqueurs
- ASF (format des systèmes avancés), marqueurs
- lecteurs asynchrones, recherche de marqueurs
- lecteurs asynchrones, marqueurs
- marqueurs, recherche
- marqueurs, lecteurs asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3361546f4087e0c2104809435d9d75e8711560ec4f3c55855d14b05ef4dfb8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807349"
---
# <a name="to-seek-to-markers"></a>Pour rechercher des marqueurs

Un marqueur est un emplacement nommé dans un fichier ASF. Vous pouvez démarrer la lecture uniquement à partir de l’emplacement d’un marqueur en utilisant le lecteur asynchrone. Vous pouvez commencer la lecture sur un marqueur en procédant comme suit.

1.  Appelez **IWMReader :: QueryInterface** pour obtenir un pointeur vers l’interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) .
2.  Récupérez le nombre total de marqueurs dans le fichier en appelant [**IWMHeaderInfo :: GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount).
3.  Parcourez les marqueurs à l’aide du nombre de marqueurs récupérés à l’étape 2. Récupérez le nom et l’heure de chaque marqueur en appelant [**IWMHeaderInfo :: GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) pour chacun d’entre eux. Enregistrez l’index du marqueur souhaité.
4.  Appelez **IWMReader :: QueryInterface** pour obtenir un pointeur vers l’interface [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) .
5.  Spécifiez le marqueur à partir duquel démarrer la lecture en appelant [**IWMReaderAdvanced2 :: StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker). Vous devez passer l’index du marqueur souhaité, que vous avez enregistré à l’étape 3.
6.  Gérez les exemples comme vous le feriez normalement dans votre implémentation de la méthode [**IWMReaderCallback :: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Marqueurs**](markers.md)
</dt> <dt>

[**Lecture des fichiers avec le lecteur asynchrone**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Utilisation des index**](working-with-indexes.md)
</dt> </dl>

 

 




