---
description: Configuration du codec MFTs
ms.assetid: 0de0cb2e-67bc-4db5-879a-95879f16b98d
title: Configuration du codec MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0065f05d10eae367b13ef6f7caf3fe2ab322163a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484097"
---
# <a name="configuring-codec-mfts"></a><span data-ttu-id="be5ad-103">Configuration du codec MFTs</span><span class="sxs-lookup"><span data-stu-id="be5ad-103">Configuring Codec MFTs</span></span>

<span data-ttu-id="be5ad-104">Cette rubrique décrit le processus de configuration du codec MFTs.</span><span class="sxs-lookup"><span data-stu-id="be5ad-104">This topic describes the process of configuring the codec MFTs.</span></span> <span data-ttu-id="be5ad-105">Chaque codec a des procédures spécifiques, mais les informations communes à toutes sont décrites ici.</span><span class="sxs-lookup"><span data-stu-id="be5ad-105">Each codec has specific procedures, but the information common to all is described here.</span></span>

## <a name="configuring-mft-inputs-and-outputs"></a><span data-ttu-id="be5ad-106">Configuration des entrées et des sorties MFT</span><span class="sxs-lookup"><span data-stu-id="be5ad-106">Configuring MFT Inputs and Outputs</span></span>

<span data-ttu-id="be5ad-107">Chaque MFT prend en charge des types d’entrée et de sortie spécifiques.</span><span class="sxs-lookup"><span data-stu-id="be5ad-107">Every MFT supports specific input and output types.</span></span> <span data-ttu-id="be5ad-108">Vous pouvez récupérer les types d’entrée pris en charge en appelant à plusieurs reprises [**IMFTransform :: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype), en incrémentant l’index de type avec chaque appel.</span><span class="sxs-lookup"><span data-stu-id="be5ad-108">You can retrieve supported input types by repeatedly calling [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype), incrementing the type index with each call.</span></span> <span data-ttu-id="be5ad-109">Lorsque vous trouvez un type approprié, définissez le type d’entrée en appelant [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span><span class="sxs-lookup"><span data-stu-id="be5ad-109">When you find an appropriate type, set the input type by calling [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span></span> <span data-ttu-id="be5ad-110">Vous pouvez ensuite répéter le processus pour le type de sortie à l’aide des appels [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) et [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="be5ad-110">You can then repeat the process for the output type using the calls [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) and [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span> <span data-ttu-id="be5ad-111">Vous devez interroger ou définir les types de sortie disponibles uniquement après avoir défini le type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="be5ad-111">You must query or set the available output types only after setting the input type.</span></span>

## <a name="configuring-the-codec-mfts-for-encoding"></a><span data-ttu-id="be5ad-112">Configuration du codec MFTs pour l’encodage</span><span class="sxs-lookup"><span data-stu-id="be5ad-112">Configuring the Codec MFTs for Encoding</span></span>

<span data-ttu-id="be5ad-113">Tous les codecs vidéo et Windows Media Audio prennent en charge un large éventail de fonctionnalités d’encodage.</span><span class="sxs-lookup"><span data-stu-id="be5ad-113">All of the Windows Media Audio and Video codecs support a variety of encoding features.</span></span> <span data-ttu-id="be5ad-114">Ces fonctionnalités sont généralement configurées en définissant des propriétés sur la table MFT à l’aide des méthodes de l’interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="be5ad-114">These features are generally configured by setting properties on the MFT by using the methods of the **IPropertyStore** interface.</span></span> <span data-ttu-id="be5ad-115">Certaines propriétés sont configurées à l’aide d’interfaces de codec spécialisées.</span><span class="sxs-lookup"><span data-stu-id="be5ad-115">Some properties are configured using specialized codec interfaces.</span></span> <span data-ttu-id="be5ad-116">Ces interfaces sont répertoriées pour chaque codec dans la section [objets codec](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="be5ad-116">These interfaces are listed for each codec in the section [Codec Objects](codecobjects.md).</span></span>

<span data-ttu-id="be5ad-117">L’ordre général des opérations de configuration d’une table MFT d’encodage est le suivant :</span><span class="sxs-lookup"><span data-stu-id="be5ad-117">The general order of operations for configuring an encoding MFT is as follows:</span></span>

1.  <span data-ttu-id="be5ad-118">Configurez les fonctionnalités du codec comme vous le souhaitez à l’aide des méthodes de **IPropertyStore**.</span><span class="sxs-lookup"><span data-stu-id="be5ad-118">Configure codec features as desired by using the methods of **IPropertyStore**.</span></span>
2.  <span data-ttu-id="be5ad-119">Utilisez les interfaces MFT du codec pour configurer des fonctionnalités supplémentaires, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="be5ad-119">Use the codec MFT interfaces to configure additional features, if needed.</span></span>
3.  <span data-ttu-id="be5ad-120">Configurez les types d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="be5ad-120">Configure the input and output types.</span></span> <span data-ttu-id="be5ad-121">L’ordre dans lequel les types doivent être configurés varie en fonction des codecs individuels.</span><span class="sxs-lookup"><span data-stu-id="be5ad-121">The order in which the types should be configured varies for individual codecs.</span></span> <span data-ttu-id="be5ad-122">Pour plus d’informations, consultez [utilisation de l’audio](workingwithaudio.md) et [utilisation de la vidéo](workingwithvideo.md).</span><span class="sxs-lookup"><span data-stu-id="be5ad-122">For more information, see [Working with Audio](workingwithaudio.md) and [Working with Video](workingwithvideo.md).</span></span>

## <a name="configuring-the-codec-mfts-for-decoding"></a><span data-ttu-id="be5ad-123">Configuration du codec MFTs pour le décodage</span><span class="sxs-lookup"><span data-stu-id="be5ad-123">Configuring the Codec MFTs for Decoding</span></span>

<span data-ttu-id="be5ad-124">Le décodage est plus simple que l’encodage, car un nombre inférieur de fonctionnalités de décodeur est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="be5ad-124">Decoding is simpler than encoding, as fewer decoder features are supported.</span></span>

<span data-ttu-id="be5ad-125">L’ordre général des opérations de configuration d’une table MFT de décodage est le suivant :</span><span class="sxs-lookup"><span data-stu-id="be5ad-125">The general order of operations for configuring a decoding MFT is as follows:</span></span>

1.  <span data-ttu-id="be5ad-126">Configurez les fonctionnalités du décodeur comme vous le souhaitez à l’aide des méthodes de **IPropertyStore**.</span><span class="sxs-lookup"><span data-stu-id="be5ad-126">Configure decoder features as desired by using the methods of **IPropertyStore**.</span></span>
2.  <span data-ttu-id="be5ad-127">Définissez le type d’entrée sur le type utilisé pour la sortie de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="be5ad-127">Set the input type to the type used for the encoder output.</span></span>
3.  <span data-ttu-id="be5ad-128">Configurez le type de sortie.</span><span class="sxs-lookup"><span data-stu-id="be5ad-128">Configure the output type.</span></span> <span data-ttu-id="be5ad-129">Les types de sortie pris en charge sont différents pour les différentes entrées.</span><span class="sxs-lookup"><span data-stu-id="be5ad-129">The supported output types are different for different inputs.</span></span>

> [!Note]  
> <span data-ttu-id="be5ad-130">Il est important d’utiliser le même type de média pour l’entrée du décodeur que celui utilisé pour la sortie de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="be5ad-130">It is important to use the same media type for the decoder input as was used for the encoder output.</span></span> <span data-ttu-id="be5ad-131">Cela est dû au fait que les codecs Windows Media Audio et vidéo utilisent des formats multimédias avec des données supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="be5ad-131">This is because the Windows Media Audio and Video codecs use media formats with extra data.</span></span> <span data-ttu-id="be5ad-132">Sans les données de format étendu, vous ne pouvez pas décoder le contenu compressé.</span><span class="sxs-lookup"><span data-stu-id="be5ad-132">Without the extended format data, you cannot decode the compressed content.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="be5ad-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be5ad-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be5ad-134">Utilisation du codec MFTs</span><span class="sxs-lookup"><span data-stu-id="be5ad-134">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



