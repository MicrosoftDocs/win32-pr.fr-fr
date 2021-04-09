---
title: Pour rechercher par numéro de frame à l’aide du lecteur asynchrone
description: Pour rechercher par numéro de frame à l’aide du lecteur asynchrone
ms.assetid: faab6344-3afc-47ff-9107-d2ce36c0a2b8
keywords:
- ASF (Advanced Systems Format), recherche par numéro de trame
- ASF (format avancé des systèmes), recherche par numéro de trame
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- lecteurs asynchrones, recherche par numéros de frame
- flux vidéo, recherche par numéros de frame
- flux vidéo, lecteurs asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 169f5e1ac1e6034bc1db6f610e80af50dd3a0215
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030787"
---
# <a name="to-seek-by-frame-number-using-the-asynchronous-reader"></a>Pour rechercher par numéro de frame à l’aide du lecteur asynchrone

L’objet lecteur asynchrone peut être utilisé pour rechercher le nombre de trames des flux vidéo dans un fichier ASF. Pour utiliser la recherche basée sur des frames, le fichier chargé dans le lecteur doit être indexé par frame. Chaque flux vidéo individuel peut être indexé. Pour déterminer si un flux a été indexé par Frame, vous pouvez vérifier l’attribut g \_ wszWMNumberOfFrames dans l’en-tête du fichier en appelant [**IWMHeaderInfo :: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).

Pour rechercher des données dans un fichier ASF par numéro de trame à l’aide du lecteur asynchrone, procédez comme suit.

1.  Obtenez un pointeur vers l’interface [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) de l’objet lecteur en appelant **IWMReader :: QueryInterface**.
2.  Définissez le numéro et la durée du frame de départ en appelant [**IWMReaderAdvanced3 :: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition). Vous devez spécifier le numéro de flux d’un flux vidéo indexé par une image. Le lecteur synchronise le reste des sorties avec l’heure de présentation du frame spécifié du flux spécifié et commence à fournir des exemples de sortie.
3.  Gérez les exemples comme vous le feriez normalement dans votre implémentation de la méthode **IWMReaderCallback :: OnSample** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecture des fichiers avec le lecteur asynchrone**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Lecture des métadonnées lors de la lecture**](reading-metadata-at-playback.md)
</dt> <dt>

[**Utilisation des index**](working-with-indexes.md)
</dt> </dl>

 

 




