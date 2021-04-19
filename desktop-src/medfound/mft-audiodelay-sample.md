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
# <a name="mft_audiodelay-sample"></a><span data-ttu-id="23e73-103">\_Exemple AUDIODELAY MFT</span><span class="sxs-lookup"><span data-stu-id="23e73-103">MFT\_AudioDelay Sample</span></span>

<span data-ttu-id="23e73-104">Montre comment implémenter un effet audio en tant que transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="23e73-104">Shows how to implement an audio effect as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="23e73-105">La table MFT de délai audio accepte les données audio PCM comme entrée, applique un effet de délai (ECHO) et génère les données audio modifiées.</span><span class="sxs-lookup"><span data-stu-id="23e73-105">The audio delay MFT accepts PCM audio as input, applies a delay (echo) effect, and outputs the modified audio data.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="23e73-106">API illustrées</span><span class="sxs-lookup"><span data-stu-id="23e73-106">APIs Demonstrated</span></span>

<span data-ttu-id="23e73-107">Cet exemple illustre les interfaces de Microsoft Media Foundation suivantes :</span><span class="sxs-lookup"><span data-stu-id="23e73-107">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="23e73-108">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="23e73-108">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a><span data-ttu-id="23e73-109">Utilisation</span><span class="sxs-lookup"><span data-stu-id="23e73-109">Usage</span></span>

<span data-ttu-id="23e73-110">L' \_ exemple AUDIODELAY MFT génère une dll qui est un serveur com pour la MFT.</span><span class="sxs-lookup"><span data-stu-id="23e73-110">The MFT\_AudioDelay sample builds a DLL that is a COM server for the MFT.</span></span> <span data-ttu-id="23e73-111">Avant d’utiliser la MFT, vous devez inscrire la DLL.</span><span class="sxs-lookup"><span data-stu-id="23e73-111">Before using the MFT, you must register the DLL.</span></span> <span data-ttu-id="23e73-112">Vous pouvez utiliser l’outil TopoEdit pour créer une topologie qui comprend la MFT de délai audio.</span><span class="sxs-lookup"><span data-stu-id="23e73-112">You can use the TopoEdit tool to build a topology that includes the audio delay MFT.</span></span> <span data-ttu-id="23e73-113">Pour plus d’informations sur TopoEdit, consultez [TopoEdit](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="23e73-113">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span> <span data-ttu-id="23e73-114">Vous pouvez également modifier l' [exemple PlaybackFX](/previous-versions//bb970336(v=vs.85)) pour utiliser la table MFT.</span><span class="sxs-lookup"><span data-stu-id="23e73-114">You can also modify the [PlaybackFX Sample](/previous-versions//bb970336(v=vs.85)) to use the MFT.</span></span> <span data-ttu-id="23e73-115">Vous devrez modifier la fonction AddBranchToPartialTopology dans Player. cpp.</span><span class="sxs-lookup"><span data-stu-id="23e73-115">You will need to modify the AddBranchToPartialTopology function in Player.cpp.</span></span> <span data-ttu-id="23e73-116">Modifiez la ligne suivante à partir de :</span><span class="sxs-lookup"><span data-stu-id="23e73-116">Change the following line from:</span></span>

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, GUID_NULL);
}
```

<span data-ttu-id="23e73-117">Par :</span><span class="sxs-lookup"><span data-stu-id="23e73-117">To:</span></span>

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, CLSID_DelayMFT);
}
```

<span data-ttu-id="23e73-118">La valeur CLSID \_ DelayMFT est déclarée dans le fichier d’en-tête AudioDelayUuids. h dans l' \_ exemple de dossier MFT AudioDelay.</span><span class="sxs-lookup"><span data-stu-id="23e73-118">The value CLSID\_DelayMFT is declared in the header file AudioDelayUuids.h in the MFT\_AudioDelay sample folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="23e73-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23e73-119">Requirements</span></span>



| <span data-ttu-id="23e73-120">Produit</span><span class="sxs-lookup"><span data-stu-id="23e73-120">Product</span></span>                                                        | <span data-ttu-id="23e73-121">Version</span><span class="sxs-lookup"><span data-stu-id="23e73-121">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="23e73-122">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="23e73-122">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="23e73-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="23e73-123">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="23e73-124">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="23e73-124">Downloading the Sample</span></span>

<span data-ttu-id="23e73-125">Cet exemple est disponible dans le [référentiel GitHub des exemples classiques Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay).</span><span class="sxs-lookup"><span data-stu-id="23e73-125">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay).</span></span>

## <a name="related-topics"></a><span data-ttu-id="23e73-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="23e73-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23e73-127">Exemples du kit de développement logiciel Media Foundation</span><span class="sxs-lookup"><span data-stu-id="23e73-127">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="23e73-128">Transformations de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="23e73-128">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="23e73-129">\_Exemple de nuances de gris MFT</span><span class="sxs-lookup"><span data-stu-id="23e73-129">MFT\_Grayscale Sample</span></span>](mft-grayscale-sample.md)
</dt> <dt>

[<span data-ttu-id="23e73-130">Écriture d’une table MFT personnalisée</span><span class="sxs-lookup"><span data-stu-id="23e73-130">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 
