---
title: Pour effectuer une recherche par heure à l’aide du lecteur asynchrone
description: Pour effectuer une recherche par heure à l’aide du lecteur asynchrone
ms.assetid: 731b0a6e-1472-45a7-998c-e395be86036f
keywords:
- ASF (Advanced Systems Format), recherche par heure
- ASF (format de systèmes avancés), recherche par heure
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- lecteurs asynchrones, recherche par heure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f3e24c04d75d762aef6bac498d4b4c8dfa9552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723563"
---
# <a name="to-seek-by-time-using-the-asynchronous-reader"></a>Pour effectuer une recherche par heure à l’aide du lecteur asynchrone

Si vous souhaitez rechercher une heure de présentation spécifique dans un fichier ASF, le fichier doit être correctement configuré. Vous pouvez rechercher des fichiers audio uniquement par défaut, mais les fichiers vidéo doivent être indexés avant la recherche. Si vous n’êtes pas sûr de la façon dont un fichier a été créé, vous pouvez vérifier l' \_ attribut g wszWMSeekable dans l’en-tête du fichier en appelant [**IWMHeaderInfo :: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).

Pour rechercher des données dans un fichier ASF par heure de présentation à l’aide du lecteur asynchrone, appelez [**IWMReader :: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), en passant la durée souhaitée et la durée de la partie du fichier que vous souhaitez lire en tant que *cnsStart* et *cnsDuration* , respectivement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Lecture des fichiers avec le lecteur asynchrone**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Lecture des métadonnées lors de la lecture**](reading-metadata-at-playback.md)
</dt> <dt>

[**Utilisation des index**](working-with-indexes.md)
</dt> </dl>

 

 




