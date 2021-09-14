---
description: Exemple WavSource
ms.assetid: 905fbba5-0a04-4048-80bd-f8707c4879da
title: Exemple WavSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050edb9df75032384f93c6e1f37c52e89f14a748
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313586"
---
# <a name="wavsource-sample"></a>Exemple WavSource

Montre comment créer une source de média personnalisée dans Microsoft Media Foundation. L’exemple implémente une source multimédia qui analyse les fichiers audio. wav.

Cet exemple est un exemple relativement simple d’une source de média :

-   Il n’existe qu’un seul flux, il n’y a donc aucun code pour implémenter la sélection de flux.
-   La source du média n’implémente pas le contrôle de la fréquence (autrement dit, la lecture rapide ou inversée).
-   Toutes les méthodes de source et de flux sont implémentées en tant que méthodes synchrones.
-   Étant donné que la partie données d’un fichier. wav est un bloc unique de données audio PCM non compressées, la source du média n’a pas besoin de lire les en-têtes de paquets ou d’analyser le flux pendant la lecture, à l’exception de la lecture de l’en-tête [**WaveFormat**](/windows/win32/api/mmreg/ns-mmreg-waveformat) initial.

Pour obtenir un exemple plus avancé d’une source de média, consultez l' [exemple MPEG1Source](mpeg1source-sample.md).

## <a name="apis-demonstrated"></a>API illustrées

Cet exemple illustre les interfaces de Media Foundation suivantes :

-   [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

## <a name="usage"></a>Usage

L’exemple WavSource génère une DLL qui est un serveur COM pour la source du média et le gestionnaire de flux d’octets de la source du média. Avant d’utiliser la source du média, vous devez inscrire la DLL.

Pour utiliser la source du média, vous pouvez exécuter le [BasicPlayback](/previous-versions//bb970475(v=vs.85)). Le programme de résolution source chargera automatiquement la source du média si vous sélectionnez un fichier. wav pour la lecture. (Si une erreur se produit, assurez-vous que vous avez correctement inscrit la DLL WavSource.)

Vous pouvez également utiliser l’outil TopoEdit pour générer une topologie de lecture qui contient la source du média. Pour plus d’informations sur TopoEdit, consultez [TopoEdit](topoedit.md).

## <a name="requirements"></a>Spécifications



| Produit                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

cet exemple est disponible dans [Windows le référentiel github exemples classiques](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples du kit de développement logiciel Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Sources multimédias](media-sources.md)
</dt> <dt>

[Exemple MPEG1Source](mpeg1source-sample.md)
</dt> <dt>

[Gestionnaires de schémas et gestionnaires de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Écriture d’une source de média personnalisée](writing-a-custom-media-source.md)
</dt> </dl>

 

 
