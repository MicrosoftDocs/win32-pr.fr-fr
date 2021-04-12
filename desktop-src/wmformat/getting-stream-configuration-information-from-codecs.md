---
title: Obtention d’informations de configuration de flux à partir de codecs
description: Obtention d’informations de configuration de flux à partir de codecs
ms.assetid: 76c734a1-6fe4-4958-8773-a65f5ced80c6
keywords:
- flux, configurations à partir de codecs
- codecs, obtention de configurations de flux à partir de
- flux, formats de codec
- codecs, formats
- flux, interface IWMCodecInfo
- IWMCodecInfo, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8657e03af97f9e4f1cae953d541c0e4369da193
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "104381677"
---
# <a name="getting-stream-configuration-information-from-codecs"></a><span data-ttu-id="a0a5d-109">Obtention d’informations de configuration de flux à partir de codecs</span><span class="sxs-lookup"><span data-stu-id="a0a5d-109">Getting Stream Configuration Information from Codecs</span></span>

<span data-ttu-id="a0a5d-110">Pour les flux audio et vidéo qui utilisent les codecs vidéo et Windows Media Audio, vous devez obtenir les valeurs des structures de configuration de flux à partir du codec que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="a0a5d-110">For audio and video streams that use the Windows Media Audio and Video codecs, you should get the values for the stream configuration structures from the codec you want to use.</span></span> <span data-ttu-id="a0a5d-111">Bien qu’il soit possible de définir ces valeurs vous-même, l’utilisation des codecs garantit que les valeurs sont exactes.</span><span class="sxs-lookup"><span data-stu-id="a0a5d-111">While it is possible to set these values yourself, using the codecs ensures that the values are accurate.</span></span> <span data-ttu-id="a0a5d-112">Vous ne devez pas modifier les valeurs de ces structures, sauf si la documentation recommande spécifiquement une modification particulière.</span><span class="sxs-lookup"><span data-stu-id="a0a5d-112">You should not alter the values in these structures unless the documentation specifically recommends a particular change.</span></span>

<span data-ttu-id="a0a5d-113">Les informations des codecs sont fournies sous la forme de formats de codec.</span><span class="sxs-lookup"><span data-stu-id="a0a5d-113">Information from the codecs comes in the form of codec formats.</span></span> <span data-ttu-id="a0a5d-114">Chaque format de codec est un format de flux unique pris en charge par le codec.</span><span class="sxs-lookup"><span data-stu-id="a0a5d-114">Each codec format is a single stream format supported by the codec.</span></span> <span data-ttu-id="a0a5d-115">Pour plus d’informations sur les formats de flux, consultez [formats](formats.md).</span><span class="sxs-lookup"><span data-stu-id="a0a5d-115">For more information about stream formats, see [Formats](formats.md).</span></span>

<span data-ttu-id="a0a5d-116">Vous pouvez demander des informations à partir des codecs Windows Media à l’aide des interfaces [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo), [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)et [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) de l’objet gestionnaire de profils.</span><span class="sxs-lookup"><span data-stu-id="a0a5d-116">You can request information from the Windows Media codecs using the [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo), [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2), and [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) interfaces of the profile manager object.</span></span> <span data-ttu-id="a0a5d-117">Pour obtenir l’interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) d’un objet de gestionnaire de profils, appelez la fonction [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="a0a5d-117">To get the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface of a profile manager object, call the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span> <span data-ttu-id="a0a5d-118">Appelez **QueryInterface** sur **IWMProfileManager** pour accéder à **IWMCodecInfo3**.</span><span class="sxs-lookup"><span data-stu-id="a0a5d-118">Call **QueryInterface** on **IWMProfileManager** to get **IWMCodecInfo3**.</span></span>

<span data-ttu-id="a0a5d-119">Les sections suivantes décrivent l’obtention des informations dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="a0a5d-119">The following sections describe how to get the information you need.</span></span>



| <span data-ttu-id="a0a5d-120">Section</span><span class="sxs-lookup"><span data-stu-id="a0a5d-120">Section</span></span>                                                                                                | <span data-ttu-id="a0a5d-121">Description</span><span class="sxs-lookup"><span data-stu-id="a0a5d-121">Description</span></span>                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0a5d-122">Pour énumérer tous les codecs Windows Media installés</span><span class="sxs-lookup"><span data-stu-id="a0a5d-122">To Enumerate All Installed Windows Media Codecs</span></span>](to-enumerate-all-installed-windows-media-codecs.md) | <span data-ttu-id="a0a5d-123">Décrit comment utiliser les méthodes des interfaces **IWMCodecInfo** et **IWMCodecInfo2** pour récupérer le nom et l’index du codec de chaque codec Windows Media installé.</span><span class="sxs-lookup"><span data-stu-id="a0a5d-123">Describes how to use the methods of the **IWMCodecInfo** and **IWMCodecInfo2** interfaces to retrieve the name and codec index of each Windows Media codec installed.</span></span> |
| [<span data-ttu-id="a0a5d-124">Pour énumérer les formats de codec</span><span class="sxs-lookup"><span data-stu-id="a0a5d-124">To Enumerate Codec Formats</span></span>](to-enumerate-codec-formats.md)                                           | <span data-ttu-id="a0a5d-125">Décrit comment obtenir des objets de configuration de flux à partir de codecs à utiliser dans vos profils.</span><span class="sxs-lookup"><span data-stu-id="a0a5d-125">Describes how to get stream configuration objects from codecs for use in your profiles.</span></span>                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="a0a5d-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0a5d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0a5d-127">**Configuration de flux**</span><span class="sxs-lookup"><span data-stu-id="a0a5d-127">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




