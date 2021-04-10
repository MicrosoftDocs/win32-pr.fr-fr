---
description: Montre comment écrire un décodeur pour Microsoft Media Foundation.
ms.assetid: 941e5400-e679-41f4-9830-3548dc6037aa
title: Exemple de décodeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd7586534876cfa7f530e675b0342a92bf46b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950897"
---
# <a name="decoder-sample"></a>Exemple de décodeur

Montre comment écrire un décodeur pour Microsoft Media Foundation.

Cet exemple implémente un décodeur vidéo simulé MPEG-1 qui affiche le code de temps de chaque image vidéo. Il ne décode pas en fait le flux binaire MPEG-1. L’illustration suivante montre la sortie vidéo du décodeur.

![capture d’écran d’une image vidéo à partir du décodeur](images/decodersample.png)

> [!Note]  
> Avant le SDK Windows pour Windows 7, cet exemple était inclus dans l' [exemple MPEG1Source](mpeg1source-sample.md).

 

## <a name="apis-demonstrated"></a>API illustrées

Cet exemple illustre les interfaces de Media Foundation suivantes :

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="requirements"></a>Configuration requise



| Produit                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible dans le [référentiel GitHub des exemples classiques Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/Decoder).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples du kit de développement logiciel Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Transformations de Media Foundation](media-foundation-transforms.md)
</dt> <dt>

[Écriture d’une table MFT personnalisée](writing-a-custom-mft.md)
</dt> </dl>

 

 



