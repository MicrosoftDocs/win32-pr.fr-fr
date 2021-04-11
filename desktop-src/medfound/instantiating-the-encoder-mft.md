---
description: Instanciation d’une table MFT d’encodeur
ms.assetid: 50b71c00-b7cf-4c38-8114-bb36b358fda5
title: Instanciation d’une table MFT d’encodeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5344c19a3a00c659efbbfd88d42176b876528380
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203870"
---
# <a name="instantiating-an-encoder-mft"></a><span data-ttu-id="6941a-103">Instanciation d’une table MFT d’encodeur</span><span class="sxs-lookup"><span data-stu-id="6941a-103">Instantiating an Encoder MFT</span></span>

<span data-ttu-id="6941a-104">Dans Microsoft Media Foundation, les encodeurs sont implémentés en tant que [transformations Media Foundation](media-foundation-transforms.md) (MFTS).</span><span class="sxs-lookup"><span data-stu-id="6941a-104">In Microsoft Media Foundation, encoders are implemented as [Media Foundation transforms](media-foundation-transforms.md) (MFTs).</span></span> <span data-ttu-id="6941a-105">Avant de créer un encodeur, vous devez d’abord Rechercher l’encodeur qui convient le mieux à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="6941a-105">Before creating an encoder, you must first find the encoder that is most suited to your needs.</span></span>

-   <span data-ttu-id="6941a-106">Codecs audio Windows Media</span><span class="sxs-lookup"><span data-stu-id="6941a-106">Windows Media audio codecs</span></span>

    <span data-ttu-id="6941a-107">Catégorie : **\_ \_ \_ encodeur audio de catégorie MFT**</span><span class="sxs-lookup"><span data-stu-id="6941a-107">Category: **MFT\_CATEGORY\_AUDIO\_ENCODER**</span></span>

    <span data-ttu-id="6941a-108">Type majeur : MFMediaType \_ audio</span><span class="sxs-lookup"><span data-stu-id="6941a-108">Major type: MFMediaType\_Audio</span></span>

    <span data-ttu-id="6941a-109">Sous-type : MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF</span><span class="sxs-lookup"><span data-stu-id="6941a-109">SubType: MFAudioFormat\_WMAudioV9, MFAudioFormat\_WMAudioV8, MFAudioFormat\_WMAudio\_Lossless, MFAudioFormat\_WMASPDIF</span></span>

-   <span data-ttu-id="6941a-110">Codecs Windows Media Video</span><span class="sxs-lookup"><span data-stu-id="6941a-110">Windows Media video codecs</span></span>

    <span data-ttu-id="6941a-111">Catégorie : **\_ \_ \_ encodeur vidéo de catégorie MFT**</span><span class="sxs-lookup"><span data-stu-id="6941a-111">Category: **MFT\_CATEGORY\_VIDEO\_ENCODER**</span></span>

    <span data-ttu-id="6941a-112">Type majeur : \_ vidéo MFMediaType</span><span class="sxs-lookup"><span data-stu-id="6941a-112">Major type: MFMediaType\_Video</span></span>

    <span data-ttu-id="6941a-113">SubType : MFVideoFormat \_ WVC1, MFVideoFormat \_ WMV3, MFVideoFormat \_ WMV2, MFVideoFormat \_ WMV1</span><span class="sxs-lookup"><span data-stu-id="6941a-113">SubType: MFVideoFormat\_WVC1, MFVideoFormat\_WMV3, MFVideoFormat\_WMV2, MFVideoFormat\_WMV1</span></span>

<span data-ttu-id="6941a-114">Media Foundation fournit plusieurs fonctions que votre application peut appeler pour énumérer les différents encodeurs disponibles dans votre système.</span><span class="sxs-lookup"><span data-stu-id="6941a-114">Media Foundation provides several functions that your application can call to enumerate the various encoders available in your system.</span></span> <span data-ttu-id="6941a-115">Les encodeurs sont enregistrés en tant qu’objets COM et l’entrée de Registre suit le format standard pour les fabriques de classes COM.</span><span class="sxs-lookup"><span data-stu-id="6941a-115">Encoders are registered as COM objects and the registry entry follows the standard format for COM class factories.</span></span> <span data-ttu-id="6941a-116">Le registre gère les CLSID des encodeurs, qui sont catégorisés par le format multimédia (audio ou vidéo).</span><span class="sxs-lookup"><span data-stu-id="6941a-116">The registry maintains the CLSIDs for the encoders, which are categorized by the media format (audio or video).</span></span> <span data-ttu-id="6941a-117">Les identificateurs de classe des encodeurs Windows Media sont définis en tant que constantes dans le fichier d’en-tête wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="6941a-117">The class identifiers of the Windows Media encoders are defined as constants in the wmcodecdsp.h header file.</span></span> <span data-ttu-id="6941a-118">Dans Media Foundation, les encodeurs peuvent être inscrits par le biais d’appels à [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) ou [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) en spécifiant le catégorie, les types d’entrée pris en charge et les types de sortie pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6941a-118">In Media Foundation, the encoders can be registered through calls to [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) or [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) by specifying the catergory, the supported input types, and the supported output types.</span></span> <span data-ttu-id="6941a-119">Une fois l’inscription réussie via ces fonctions, les MFTs sont considérés par les fonctions d’énumération Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6941a-119">Upon successful registration through these functions, the MFTs are considered by the Media Foundation enumeration functions.</span></span>

<span data-ttu-id="6941a-120">Pour créer une instance d’une table MFT d’encodeur, une application peut choisir les options suivantes.</span><span class="sxs-lookup"><span data-stu-id="6941a-120">For creating an instance of an encoder MFT, an application has the following choices.</span></span>

-   <span data-ttu-id="6941a-121">Créez directement la MFT de l’encodeur et recevez un pointeur vers l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="6941a-121">Create the encoder MFT directly and receive a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span> <span data-ttu-id="6941a-122">Pour plus d’informations, consultez [création d’un encodeur à l’aide de CoCreateInstance](using-an-encoder-s-imftransform--interface.md).</span><span class="sxs-lookup"><span data-stu-id="6941a-122">For more information, see [Creating an Encoder by Using CoCreateInstance](using-an-encoder-s-imftransform--interface.md).</span></span>
-   <span data-ttu-id="6941a-123">Créez une instance de l’objet d’activation pour la table MFT de l’encodeur et recevez un pointeur vers l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="6941a-123">Create an instance of the activation object for the encoder MFT and receive a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span> <span data-ttu-id="6941a-124">Pour plus d’informations, consultez [utilisation des objets d’activation d’un encodeur](using-an-encoder-s-activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6941a-124">For more information, see [Using an Encoder's Activation Objects](using-an-encoder-s-activation-objects.md).</span></span>

<span data-ttu-id="6941a-125">Si votre application utilise des [composants ASF de couche de pipeline](pipeline-layer-asf-components.md) pour encoder un fichier au format ASF, vous devez insérer la table MFT de l’encodeur dans le pipeline en tant que nœud de transformation.</span><span class="sxs-lookup"><span data-stu-id="6941a-125">If your application is using [Pipeline Layer ASF Components](pipeline-layer-asf-components.md) to encode a file to ASF format, you must insert the encoder MFT into the pipeline as a transform node.</span></span> <span data-ttu-id="6941a-126">Lors de la création du nœud transformer dans la topologie d’encodage, vous pouvez soit définir le type d’objet en tant que pointeur vers l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) , soit l’objet [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="6941a-126">While creating the transform node in the encoding topology, you can either set the object type as a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface or the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object.</span></span> <span data-ttu-id="6941a-127">Media Foundation fournit des objets d’activation pour les encodeurs Windows Media afin qu’ils puissent être définis facilement comme nœud de transformation dans la topologie d’encodage.</span><span class="sxs-lookup"><span data-stu-id="6941a-127">Media Foundation provides activation objects for Windows Media encoders so that they can be conveniently set as the transform node in the encoding topology.</span></span> <span data-ttu-id="6941a-128">Lorsque la topologie est résolue, la session multimédia utilise l’objet d’activation pour créer une instance de la MFT de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="6941a-128">When the topology is resolved, the Media Session uses the activation object to create an instance of the encoder MFT.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6941a-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6941a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6941a-130">Encodeurs Windows Media</span><span class="sxs-lookup"><span data-stu-id="6941a-130">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



