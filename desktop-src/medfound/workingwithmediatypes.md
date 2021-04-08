---
description: Utilisation des types de médias DMO
ms.assetid: 1aaf7554-1a5f-439a-afb1-a031607e1a1e
title: Utilisation des types de médias DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db172538280a5dcdc6f4ffe91c19ac1d51e91ef9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953373"
---
# <a name="working-with-dmo-media-types"></a><span data-ttu-id="12dce-103">Utilisation des types de médias DMO</span><span class="sxs-lookup"><span data-stu-id="12dce-103">Working with DMO Media Types</span></span>

<span data-ttu-id="12dce-104">Les types de médias d’entrée et de sortie utilisés par le codec DMOs sont définis à l’aide de la structure de [**\_ \_ type de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) .</span><span class="sxs-lookup"><span data-stu-id="12dce-104">The input and output media types that are used by the codec DMOs are defined using the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure.</span></span> <span data-ttu-id="12dce-105">Cette structure est identique au [**type de \_ média \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type), qui est défini dans le kit de développement logiciel (SDK) du format Windows Media et au [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type), qui est défini dans Microsoft DirectShow®.</span><span class="sxs-lookup"><span data-stu-id="12dce-105">This structure is identical to both [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type), which is defined in the Windows Media Format SDK, and [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type), which is defined in Microsoft DirectShow®.</span></span> <span data-ttu-id="12dce-106">Selon votre application, vous pouvez utiliser des variables définies comme l’un de ces trois types.</span><span class="sxs-lookup"><span data-stu-id="12dce-106">Depending upon your application, you may use variables defined as any one of these three types.</span></span> <span data-ttu-id="12dce-107">Il est possible d’effectuer un cast en toute sécurité d’un pointeur vers l’une des structures de type de média en tant qu’autre.</span><span class="sxs-lookup"><span data-stu-id="12dce-107">It is safe to cast a pointer to one of the media type structures as another.</span></span> <span data-ttu-id="12dce-108">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="12dce-108">For example:</span></span>


```
    DMO_MEDIA_TYPE MediaType;
    WM_MEDIA_TYPE* pMedia = NULL;
    pMedia = (WM_MEDIA_TYPE*)&MediaType;
```



<span data-ttu-id="12dce-109">Les types de format utilisés par les codecs sont généralement limités à ceux décrits par les structures **VIDEOINFOHEADER** et **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="12dce-109">The format types that are used by the codecs are generally limited to those described by the **VIDEOINFOHEADER** and **WAVEFORMATEX** structures.</span></span> <span data-ttu-id="12dce-110">Pour plus de commodité, les constantes pour ces types de format sont incluses dans le fichier d’en-tête wmcodecconst. h.</span><span class="sxs-lookup"><span data-stu-id="12dce-110">For convenience, constants for these format types are included in the wmcodecconst.h header file.</span></span> <span data-ttu-id="12dce-111">Les noms de constantes sont \_ respectivement WMCFORMAT videoinfo et WMCFORMAT \_ WaveFormatEx.</span><span class="sxs-lookup"><span data-stu-id="12dce-111">The constant names are WMCFORMAT\_VideoInfo and WMCFORMAT\_WaveFormatEx respectively.</span></span> <span data-ttu-id="12dce-112">Les codecs audio peuvent fonctionner avec la structure **WAVEFORMATEXTENSIBLE** dans certains cas, et doivent les utiliser dans d’autres.</span><span class="sxs-lookup"><span data-stu-id="12dce-112">The audio codecs can work with the **WAVEFORMATEXTENSIBLE** structure in some circumstances, and must use it in others.</span></span> <span data-ttu-id="12dce-113">Toutefois, **DMO \_ Media \_ type. formatType** est défini sur la même valeur que pour **WAVEFORMATEX**.</span><span class="sxs-lookup"><span data-stu-id="12dce-113">However, **DMO\_MEDIA\_TYPE.formattype** is set to the same value as it is for **WAVEFORMATEX**.</span></span> <span data-ttu-id="12dce-114">Pour plus d’informations sur l’utilisation de **WAVEFORMATEXTENSIBLE**, consultez [utilisation de l’audio High-Definition](usinghighdefinitionaudio.md).</span><span class="sxs-lookup"><span data-stu-id="12dce-114">For more information about using **WAVEFORMATEXTENSIBLE**, see [Using High-Definition Audio](usinghighdefinitionaudio.md).</span></span>

> [!Note]  
>    <span data-ttu-id="12dce-115">Vous devez inclure la structure de type de format utilisée comme sortie de l’encodeur dans le conteneur que vous utilisez pour stocker les données compressées.</span><span class="sxs-lookup"><span data-stu-id="12dce-115">You must include the format type structure used as the encoder output in whatever container you use to store the compressed data.</span></span> <span data-ttu-id="12dce-116">Les décodeurs nécessitent la structure de format d’origine pour décompresser le contenu.</span><span class="sxs-lookup"><span data-stu-id="12dce-116">The decoders require the original format structure to decompress the content.</span></span> <span data-ttu-id="12dce-117">Outre les membres de la structure, les Windows Media Audio et les types de vidéo compressés requièrent des informations de format supplémentaires, qui sont ajoutées à la structure.</span><span class="sxs-lookup"><span data-stu-id="12dce-117">In addition to the members of the structure, compressed Windows Media Audio and Video types require additional format information, which is appended to the structure.</span></span> <span data-ttu-id="12dce-118">Pour plus d’informations, consultez [utilisation de l’audio](workingwithaudio.md) et [utilisation de la vidéo](workingwithvideo.md).</span><span class="sxs-lookup"><span data-stu-id="12dce-118">For more information, see [Working with Audio](workingwithaudio.md) and [Working with Video](workingwithvideo.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="12dce-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="12dce-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12dce-120">Utilisation du codec DMOs</span><span class="sxs-lookup"><span data-stu-id="12dce-120">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 
