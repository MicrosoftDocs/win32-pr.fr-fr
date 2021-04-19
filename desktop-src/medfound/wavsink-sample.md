---
description: Exemple WavSink
ms.assetid: 9e1af25f-d55c-45db-8c76-abf814e16700
title: Exemple WavSink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e96ecca551b6ea3e6837f211f0afcb34818d635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524581"
---
# <a name="wavsink-sample"></a>Exemple WavSink

Montre comment implémenter un récepteur multimédia personnalisé dans Microsoft Media Foundation. L’exemple implémente un récepteur d’archive qui écrit des données audio PCM non compressées dans un fichier. wav.

## <a name="apis-demonstrated"></a>API illustrées

Cet exemple illustre les interfaces de Media Foundation suivantes :

-   [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)
-   [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
-   [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)

## <a name="usage"></a>Utilisation

L’exemple WavSink contient deux projets Visual Studio :

-   WavSink. vcproj génère une bibliothèque statique qui contient l’implémentation du récepteur multimédia.
-   WriteWavFile. vcproj génère une application console qui utilise le récepteur multimédia pour produire un fichier. wav. Cette application est liée à la bibliothèque créée par le projet WavSink.

## <a name="requirements"></a>Configuration requise



| Produit                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible dans le [référentiel GitHub des exemples classiques Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples du kit de développement logiciel Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Récepteurs de médias](media-sinks.md)
</dt> </dl>

 

 



