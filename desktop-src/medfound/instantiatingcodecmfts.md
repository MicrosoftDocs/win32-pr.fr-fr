---
description: Instanciation du codec MFTs
ms.assetid: 171f9a0f-effb-4ed7-8aff-d7b1ee6e4973
title: Instanciation du codec MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa886f24f7dbd1acc373c7e505baddf71bc3aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201533"
---
# <a name="instantiating-codec-mfts"></a><span data-ttu-id="4bb9a-103">Instanciation du codec MFTs</span><span class="sxs-lookup"><span data-stu-id="4bb9a-103">Instantiating Codec MFTs</span></span>

<span data-ttu-id="4bb9a-104">Les [transformations de Media Foundation](media-foundation-transforms.md) (MFTS) sont des objets COM qui implémentent l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="4bb9a-104">[Media Foundation Transforms](media-foundation-transforms.md) (MFTs) are COM objects that implement the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span> <span data-ttu-id="4bb9a-105">Une table MFT est un objet permettant de transformer des données multimédias dans le cadre d’un pipeline.</span><span class="sxs-lookup"><span data-stu-id="4bb9a-105">An MFT is an object for transforming multimedia data as part of a pipeline.</span></span> <span data-ttu-id="4bb9a-106">Un pipeline est un graphique acycliques dirigé, qui se compose de sources multimédias, de transformations multimédia et de récepteurs multimédias.</span><span class="sxs-lookup"><span data-stu-id="4bb9a-106">A pipeline is a directed acyclic graph, consisting of media sources, media transforms, and media sinks.</span></span> <span data-ttu-id="4bb9a-107">Un pipeline traite la diffusion en continu de données multimédias de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="4bb9a-107">A pipeline processes streaming multimedia data asynchronously.</span></span>

<span data-ttu-id="4bb9a-108">Bien que MFTs puisse être instancié et utilisé indépendamment de l’infrastructure de pipeline Media Foundation, il est préférable d’utiliser l’infrastructure MediaFoundation dans la mesure du possible.</span><span class="sxs-lookup"><span data-stu-id="4bb9a-108">Although MFTs can be instantiated and used independently of the Media Foundation pipeline infrastructure, it is preferable to use the MediaFoundation framework where possible.</span></span>

<span data-ttu-id="4bb9a-109">Vous pouvez créer une table MFT de codec en appelant la fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="4bb9a-109">You can create a codec MFT by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span> <span data-ttu-id="4bb9a-110">Vous devez passer l’identificateur de classe de la table MFT, l’identificateur d’interface de [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)et un pointeur vers un pointeur **IMFTransform** .</span><span class="sxs-lookup"><span data-stu-id="4bb9a-110">You must pass the class identifier of the MFT, the interface identifier of [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform), and a pointer to an **IMFTransform** pointer.</span></span>

<span data-ttu-id="4bb9a-111">Les identificateurs de classe du codec MFTs sont définis en tant que constantes dans le fichier d’en-tête wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="4bb9a-111">The class identifiers of the codec MFTs are defined as constants in the wmcodecdsp.h header file.</span></span>

<span data-ttu-id="4bb9a-112">La constante de l’identificateur d’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) est IID \_ IMFTransform.</span><span class="sxs-lookup"><span data-stu-id="4bb9a-112">The constant for the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface identifier is IID\_IMFTransform.</span></span>

<span data-ttu-id="4bb9a-113">L’exemple de code suivant montre comment créer une instance d’une table MFT de codec :</span><span class="sxs-lookup"><span data-stu-id="4bb9a-113">The following code example demonstrates how to create an instance of a codec MFT:</span></span>


```
HRESULT CreateVideoEncoderMFT(IMFTransform** ppMFT)
{
    if (ppMFT == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMFTransform, 
                            (void**)ppMFT);
}
```



## <a name="related-topics"></a><span data-ttu-id="4bb9a-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4bb9a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bb9a-115">Utilisation du codec MFTs</span><span class="sxs-lookup"><span data-stu-id="4bb9a-115">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 
