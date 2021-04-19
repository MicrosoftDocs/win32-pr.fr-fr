---
description: '\_Exemple AUDIODELAY MFT'
ms.assetid: 08f119f9-cacd-4000-96b6-60c8c0055e9c
title: Exemple de MFT_AudioDelay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d382ce7d1c5e9475bef85f11ef9754345e123b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518587"
---
# <a name="mft_audiodelay-sample"></a>\_Exemple AUDIODELAY MFT

Montre comment implémenter un effet audio en tant que transformation de Media Foundation (MFT). La table MFT de délai audio accepte les données audio PCM comme entrée, applique un effet de délai (ECHO) et génère les données audio modifiées.

## <a name="apis-demonstrated"></a>API illustrées

Cet exemple illustre les interfaces de Microsoft Media Foundation suivantes :

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a>Utilisation

L' \_ exemple AUDIODELAY MFT génère une dll qui est un serveur com pour la MFT. Avant d’utiliser la MFT, vous devez inscrire la DLL. Vous pouvez utiliser l’outil TopoEdit pour créer une topologie qui comprend la MFT de délai audio. Pour plus d’informations sur TopoEdit, consultez [TopoEdit](topoedit.md). Vous pouvez également modifier l' [exemple PlaybackFX](/previous-versions//bb970336(v=vs.85)) pour utiliser la table MFT. Vous devrez modifier la fonction AddBranchToPartialTopology dans Player. cpp. Modifiez la ligne suivante à partir de :

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, GUID_NULL);
}
```

Par :

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, CLSID_DelayMFT);
}
```

La valeur CLSID \_ DelayMFT est déclarée dans le fichier d’en-tête AudioDelayUuids. h dans l' \_ exemple de dossier MFT AudioDelay.

## <a name="requirements"></a>Configuration requise



| Produit                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible dans le [référentiel GitHub des exemples classiques Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples du kit de développement logiciel Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Transformations de Media Foundation](media-foundation-transforms.md)
</dt> <dt>

[\_Exemple de nuances de gris MFT](mft-grayscale-sample.md)
</dt> <dt>

[Écriture d’une table MFT personnalisée](writing-a-custom-mft.md)
</dt> </dl>

 

 
