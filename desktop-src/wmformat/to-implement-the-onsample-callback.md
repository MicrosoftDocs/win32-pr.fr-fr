---
title: Pour implémenter le rappel OnSample
description: Pour implémenter le rappel OnSample
ms.assetid: 83bce8ee-6ce8-4079-9c87-2314824b1946
keywords:
- ASF (Advanced Systems Format), implémentation du rappel OnStatus
- ASF (format avancé des systèmes), implémentation du rappel OnStatus
- ASF (Advanced Systems Format), rappel OnStatus
- ASF (format avancé des systèmes), rappel OnStatus
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- lecteurs asynchrones, implémenter le rappel OnStatus
- OnStatus, méthode de rappel, implémentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00523ae28ec14feefb8249ff86a2b1600629c84cb245eb627b59b619a28a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027287"
---
# <a name="to-implement-the-onsample-callback"></a>Pour implémenter le rappel OnSample

Le lecteur asynchrone fournit des exemples à l’application de contrôle dans l’ordre de la présentation en effectuant des appels à la méthode de rappel [**IWMReaderCallback :: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) . Quand vous créez une application à l’aide du lecteur asynchrone, vous devez implémenter **OnSample** pour gérer les exemples non compressés. En règle générale, les fonctions ou les méthodes créées pour afficher le contenu sont appelées à partir de **OnSample**.

L’implémentation classique du rappel **OnSample** comprend les étapes suivantes.

1.  Récupérez l’emplacement et la taille de la mémoire tampon contenant l’exemple en appelant [**INSSBuffer :: GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) sur la mémoire tampon transmise en tant que *pSample*.
2.  Créer une branche de votre logique en fonction du numéro de sortie. Le numéro de sortie est passé à **OnSample** en tant que *dwOutputNumber*.
3.  Incluez la logique de rendu pour chaque numéro de sortie que vous souhaitez prendre en charge. Si vous affichez des exemples à partir de plusieurs sorties, vous devrez peut-être synchroniser votre rendu.

Les applications qui fournissent des échantillons compressés à partir de fichiers ASF doivent implémenter la méthode de rappel [**IWMReaderCallbackAdvanced :: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) . **OnStreamSample** fonctionne presque de la même façon que **OnSample**, à ceci près qu’il reçoit des échantillons compressés par numéro de flux au lieu d’exemples non compressés par numéro de sortie.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)
</dt> <dt>

[**Interface IWMReaderCallbackAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[**Lecture des fichiers avec le lecteur asynchrone**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Utilisation des méthodes de rappel**](using-the-callback-methods.md)
</dt> </dl>

 

 




