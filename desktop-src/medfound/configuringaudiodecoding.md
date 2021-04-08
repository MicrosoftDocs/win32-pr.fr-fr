---
description: Configuration du décodage audio
ms.assetid: 362bd3bc-1474-4132-a8a8-e5dc0bba80e7
title: Configuration du décodage audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da4d6a9d41b5c504ff60f25db20265072218caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749332"
---
# <a name="configuring-audio-decoding-microsoft-media-foundation"></a><span data-ttu-id="a2ff8-103">Configuration du décodage audio (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="a2ff8-103">Configuring Audio Decoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="a2ff8-104">Le décodage de contenu Windows Media Audio est beaucoup plus facile que son encodage.</span><span class="sxs-lookup"><span data-stu-id="a2ff8-104">Decoding Windows Media Audio content is much easier than encoding it.</span></span> <span data-ttu-id="a2ff8-105">Après avoir créé un objet décodeur audio, définissez le type d’entrée à l’aide de la méthode **IMediaObject :: SetInputType** ou **IMFTransform :: SetInputType** .</span><span class="sxs-lookup"><span data-stu-id="a2ff8-105">After creating an audio decoder object, set the input type by using the **IMediaObject::SetInputType** or **IMFTransform::SetInputType** method.</span></span> <span data-ttu-id="a2ff8-106">Le type de média que vous utilisez pour l’entrée du décodeur doit correspondre au type de sortie qui a été utilisé lors de l’encodage du contenu.</span><span class="sxs-lookup"><span data-stu-id="a2ff8-106">The media type that you use for the decoder input must match the output type that was used when the content was encoded.</span></span> <span data-ttu-id="a2ff8-107">Cela comprend les données de format étendu ajoutées à la structure **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="a2ff8-107">This includes the extended format data appended to the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="a2ff8-108">Vous devez vous assurer que ces données sont correctes, car le décodeur ne peut pas traiter les exemples sans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="a2ff8-108">You must ensure that this data is correct, because the decoder cannot process samples without it.</span></span>

<span data-ttu-id="a2ff8-109">Après avoir défini le type d’entrée, vous pouvez configurer les fonctionnalités de décodeur que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="a2ff8-109">After setting the input type, you can configure any decoder features you want to use.</span></span> <span data-ttu-id="a2ff8-110">Les fonctionnalités de décodeur, comme celles utilisées pour l’encodage, sont définies à l’aide des méthodes de **IPropertyBag** ou **IPropertyStore**.</span><span class="sxs-lookup"><span data-stu-id="a2ff8-110">Decoder features, like those used for encoding, are set using the methods of **IPropertyBag** or **IPropertyStore**.</span></span>

<span data-ttu-id="a2ff8-111">Une fois que le type d’entrée est défini et que toutes les fonctionnalités du décodeur sont configurées, vous pouvez énumérer les types de sortie pris en charge par le décodeur en effectuant des appels à **IMediaObject :: GetOutputType** ou **IMFTransform :: GetOutputType**.</span><span class="sxs-lookup"><span data-stu-id="a2ff8-111">After the input type is set and all decoder features are configured, you can enumerate the output types supported by the decoder by making calls to **IMediaObject::GetOutputType** or **IMFTransform::GetOutputType**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2ff8-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a2ff8-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2ff8-113">Utilisation de l’audio</span><span class="sxs-lookup"><span data-stu-id="a2ff8-113">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



