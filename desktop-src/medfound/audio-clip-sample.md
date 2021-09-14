---
description: Montre comment utiliser Microsoft Media Foundation pour décoder l’audio d’un fichier multimédia.
ms.assetid: 29822e6b-8598-4133-b181-7fb0854553b7
title: Exemple de clip audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0e4a3e515d08e2cafd2ab2ba451a528f3d5677
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127236375"
---
# <a name="audio-clip-sample"></a>Exemple de clip audio

Montre comment utiliser Microsoft Media Foundation pour décoder l’audio d’un fichier multimédia.

L’exemple d’application de clip audio lit les données audio à partir d’un fichier multimédia et écrit le contenu audio non compressé dans un fichier WAVE.

## <a name="apis-demonstrated"></a>API illustrées

Cet exemple illustre les interfaces de Media Foundation suivantes :

-   [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)

## <a name="usage"></a>Usage

Cet exemple est une application en ligne de commande. Elle utilise les arguments de ligne de commande suivants :

``` syntax
audioclip.exe inputfile outputfile.wav
```

-   FichierEntrée : nom d’un fichier qui contient un flux audio.
-   FichierSortie. wav : nom du fichier. WAVE à écrire.

## <a name="requirements"></a>Spécifications



| Produit                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

cet exemple est disponible dans [Windows le référentiel github exemples classiques](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples du kit de développement logiciel Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Lecteur source](source-reader.md)
</dt> <dt>

[Didacticiel : décodage de l’audio](tutorial--decoding-audio.md)
</dt> </dl>

 

 



