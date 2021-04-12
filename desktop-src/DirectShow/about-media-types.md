---
description: À propos des types de média
ms.assetid: 9984ba36-4e43-4886-a073-34b330274c9c
title: À propos des types de média (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3289a37e95bf5dbd1e5c277b5799a2c7c8c90586
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321469"
---
# <a name="about-media-types-directshow"></a><span data-ttu-id="37c30-103">À propos des types de média (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="37c30-103">About Media Types (DirectShow)</span></span>

<span data-ttu-id="37c30-104">Étant donné que DirectShow est modulaire, il nécessite un moyen de décrire le format des données à chaque point du graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="37c30-104">Because DirectShow is modular, it requires a way to describe the format of the data at each point in the filter graph.</span></span> <span data-ttu-id="37c30-105">Par exemple, envisagez la lecture AVI.</span><span class="sxs-lookup"><span data-stu-id="37c30-105">For example, consider AVI playback.</span></span> <span data-ttu-id="37c30-106">Les données entrent dans le graphique sous forme de flux de blocs RIFF.</span><span class="sxs-lookup"><span data-stu-id="37c30-106">Data enters the graph as a stream of RIFF chunks.</span></span> <span data-ttu-id="37c30-107">Celles-ci sont analysées dans des flux vidéo et audio.</span><span class="sxs-lookup"><span data-stu-id="37c30-107">These are parsed into video and audio streams.</span></span> <span data-ttu-id="37c30-108">Le flux vidéo est constitué de trames vidéo, qui sont probablement compressées.</span><span class="sxs-lookup"><span data-stu-id="37c30-108">The video stream consists of video frames, which are probably compressed.</span></span> <span data-ttu-id="37c30-109">Après le décodage, le flux vidéo est une série de bitmaps non compressées.</span><span class="sxs-lookup"><span data-stu-id="37c30-109">After decoding, the video stream is a series of uncompressed bitmaps.</span></span> <span data-ttu-id="37c30-110">Le flux audio passe par un processus similaire.</span><span class="sxs-lookup"><span data-stu-id="37c30-110">The audio stream goes through a similar process.</span></span>

<span data-ttu-id="37c30-111">Types de médias : Comment DirectShow représente les formats</span><span class="sxs-lookup"><span data-stu-id="37c30-111">Media Types: How DirectShow Represents Formats</span></span>

<span data-ttu-id="37c30-112">Le *type de média* est un moyen universel et extensible de décrire les formats multimédias numériques.</span><span class="sxs-lookup"><span data-stu-id="37c30-112">The *media type* is a universal and extensible way to describe digital media formats.</span></span> <span data-ttu-id="37c30-113">Lorsque deux filtres se connectent, ils s’accordent sur un type de support.</span><span class="sxs-lookup"><span data-stu-id="37c30-113">When two filters connect, they agree on a media type.</span></span> <span data-ttu-id="37c30-114">Le type de média identifie le type de données que le filtre en amont va remettre au filtre en aval et la disposition physique des données.</span><span class="sxs-lookup"><span data-stu-id="37c30-114">The media type identifies what kind of data the upstream filter will deliver to the downstream filter, and the physical layout of the data.</span></span> <span data-ttu-id="37c30-115">Si deux filtres ne peuvent pas s’accorder sur un type de média, ils ne se connectent pas.</span><span class="sxs-lookup"><span data-stu-id="37c30-115">If two filters cannot agree on a media type, they will not connect.</span></span>

<span data-ttu-id="37c30-116">Pour certaines applications, vous n’aurez jamais à vous soucier des types de médias.</span><span class="sxs-lookup"><span data-stu-id="37c30-116">For some applications, you will never have to worry about media types.</span></span> <span data-ttu-id="37c30-117">Dans la lecture de fichier, par exemple, DirectShow gère tous les détails.</span><span class="sxs-lookup"><span data-stu-id="37c30-117">In file playback, for example, DirectShow handles all of the details.</span></span> <span data-ttu-id="37c30-118">D’autres types d’applications peuvent avoir besoin de travailler directement avec les types de média.</span><span class="sxs-lookup"><span data-stu-id="37c30-118">Other kinds of applications may need to work directly with media types.</span></span>

<span data-ttu-id="37c30-119">Les types de média sont définis à l’aide de la structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="37c30-119">Media types are defined using the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="37c30-120">Cette structure contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="37c30-120">This structure contains the following information:</span></span>

-   <span data-ttu-id="37c30-121">**Type majeur**: le type principal est un GUID qui définit la catégorie globale des données.</span><span class="sxs-lookup"><span data-stu-id="37c30-121">**Major type**: The major type is a GUID that defines the overall category of the data.</span></span> <span data-ttu-id="37c30-122">Les types principaux incluent la vidéo, l’audio, le flux d’octets non analysés, les données MIDI, etc.</span><span class="sxs-lookup"><span data-stu-id="37c30-122">Major types include video, audio, unparsed byte stream, MIDI data, and so forth.</span></span>
-   <span data-ttu-id="37c30-123">**SubType**: le sous-type est un autre GUID, qui définit le format de manière plus approfondie.</span><span class="sxs-lookup"><span data-stu-id="37c30-123">**Subtype**: The subtype is another GUID, which further defines the format.</span></span> <span data-ttu-id="37c30-124">Par exemple, dans le type principal vidéo, il existe des sous-types pour RGB-24, RGB-32, UYVY, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="37c30-124">For example, within the video major type, there are subtypes for RGB-24, RGB-32, UYVY, and so forth.</span></span> <span data-ttu-id="37c30-125">Dans l’audio, il y a des données audio PCM, une charge utile MPEG-1, et d’autres.</span><span class="sxs-lookup"><span data-stu-id="37c30-125">Within audio, there is PCM audio, MPEG-1 payload, and others.</span></span> <span data-ttu-id="37c30-126">Le sous-type fournit plus d’informations que le type principal, mais il ne définit pas tout ce qui concerne le format.</span><span class="sxs-lookup"><span data-stu-id="37c30-126">The subtype provides more information than the major type, but it does not define everything about the format.</span></span> <span data-ttu-id="37c30-127">Par exemple, les sous-types vidéo ne définissent pas la taille de l’image ni la fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="37c30-127">For example, video subtypes do not define the image size or the frame rate.</span></span> <span data-ttu-id="37c30-128">Celles-ci sont définies par le bloc de format, décrit ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="37c30-128">These are defined by the format block, described below.</span></span>
-   <span data-ttu-id="37c30-129">**Bloc de format**: le bloc de format est un bloc de données qui décrit le format en détail.</span><span class="sxs-lookup"><span data-stu-id="37c30-129">**Format block**: The format block is a block of data that describes the format in detail.</span></span> <span data-ttu-id="37c30-130">Le bloc de format est alloué séparément de la structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="37c30-130">The format block is allocated separately from the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="37c30-131">Le membre **pbFormat** de la structure du **\_ \_ type de média am** pointe vers le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="37c30-131">The **pbFormat** member of the **AM\_MEDIA\_TYPE** structure points to the format block.</span></span>

    <span data-ttu-id="37c30-132">Le membre **pbFormat** est typé \**void \** _, car la disposition du bloc de format change en fonction du type de média.</span><span class="sxs-lookup"><span data-stu-id="37c30-132">The **pbFormat** member is typed \**void\** _ because the layout of the format block changes depending on the media type.</span></span> <span data-ttu-id="37c30-133">Par exemple, le son PCM utilise une structure [_ *WAVEFORMATEX* \*](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="37c30-133">For example, PCM audio uses a [_ *WAVEFORMATEX*\*](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="37c30-134">La vidéo utilise différentes structures, notamment [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) et [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span><span class="sxs-lookup"><span data-stu-id="37c30-134">Video uses various structures, including [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span> <span data-ttu-id="37c30-135">Le membre **formatType** de la structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) est un GUID qui spécifie la structure contenue dans le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="37c30-135">The **formattype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure is a GUID that specifies which structure is contained in the format block.</span></span> <span data-ttu-id="37c30-136">Un GUID est assigné à chaque structure de format.</span><span class="sxs-lookup"><span data-stu-id="37c30-136">Each format structure is assigned a GUID.</span></span> <span data-ttu-id="37c30-137">Le membre **cbFormat** spécifie la taille du bloc de format.</span><span class="sxs-lookup"><span data-stu-id="37c30-137">The **cbFormat** member specifies the size of the format block.</span></span> <span data-ttu-id="37c30-138">Vérifiez toujours ces valeurs avant de déréférencer le pointeur **pbFormat** .</span><span class="sxs-lookup"><span data-stu-id="37c30-138">Always check these values before dereferencing the **pbFormat** pointer.</span></span>

<span data-ttu-id="37c30-139">Si le bloc de format est rempli, le type et le sous-type principaux contiennent des informations redondantes.</span><span class="sxs-lookup"><span data-stu-id="37c30-139">If the format block is filled in, then the major type and subtype contain redundant information.</span></span> <span data-ttu-id="37c30-140">Toutefois, le type et le sous-type majeurs offrent un moyen pratique d’identifier des formats sans bloc de format complet.</span><span class="sxs-lookup"><span data-stu-id="37c30-140">The major type and subtype, however, provide a convenient way to identify formats without a complete format block.</span></span> <span data-ttu-id="37c30-141">Par exemple, vous pouvez spécifier un format RGB 24 bits générique (MEDIASUBTYPE \_ Rgb24), sans connaître toutes les informations requises par la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , telles que la taille de l’image et la fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="37c30-141">For example, you can specify a generic 24-bit RGB format (MEDIASUBTYPE\_RGB24), without knowing all of the information required by the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, such as image size and frame rate.</span></span>

<span data-ttu-id="37c30-142">Par exemple, un filtre peut utiliser le code suivant pour vérifier un type de média :</span><span class="sxs-lookup"><span data-stu-id="37c30-142">For example, a filter might use the following code to check a media type:</span></span>


```C++
HRESULT CheckMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt == NULL) return E_POINTER;

    // Check the major type. We're looking for video.
    if (pmt->majortype != MEDIATYPE_Video)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the subtype. We're looking for 24-bit RGB.
    if (pmt->subtype != MEDIASUBTYPE_RGB24)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the format type and the size of the format block.
    if ((pmt->formattype == FORMAT_VideoInfo) &&
         (pmt->cbFormat >= sizeof(VIDEOINFOHEADER) &&
         (pmt->pbFormat != NULL))
    {
        // Now it's safe to coerce the format block pointer to the
        // correct structure, as defined by the formattype GUID.
        VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    
        // Examine pVIH (not shown). If it looks OK, return S_OK.
        return S_OK;
    }

    return VFW_E_INVALIDMEDIATYPE;
}
```



<span data-ttu-id="37c30-143">La structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) contient également des champs facultatifs.</span><span class="sxs-lookup"><span data-stu-id="37c30-143">The [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure also contains some optional fields.</span></span> <span data-ttu-id="37c30-144">Ils peuvent être utilisés pour fournir des informations supplémentaires, mais les filtres ne sont pas requis pour les utiliser :</span><span class="sxs-lookup"><span data-stu-id="37c30-144">These can be used to provide additional information, but filters are not required to use them:</span></span>

-   <span data-ttu-id="37c30-145">**lSampleSize**.</span><span class="sxs-lookup"><span data-stu-id="37c30-145">**lSampleSize**.</span></span> <span data-ttu-id="37c30-146">Si ce champ est différent de zéro, il définit la taille de chaque échantillon.</span><span class="sxs-lookup"><span data-stu-id="37c30-146">If this field is non-zero, it defines the size of each sample.</span></span> <span data-ttu-id="37c30-147">Si la valeur est égale à zéro, cela signifie que la taille de l’échantillon peut varier de sample à Sample.</span><span class="sxs-lookup"><span data-stu-id="37c30-147">If it is zero, it indicates that the sample size may change from sample to sample.</span></span>
-   <span data-ttu-id="37c30-148">**bFixedSizeSamples**.</span><span class="sxs-lookup"><span data-stu-id="37c30-148">**bFixedSizeSamples**.</span></span> <span data-ttu-id="37c30-149">Si cet indicateur booléen a la valeur **true**, cela signifie que la valeur de **lSampleSize** est valide.</span><span class="sxs-lookup"><span data-stu-id="37c30-149">If this Boolean flag is **TRUE**, it means the value in **lSampleSize** is valid.</span></span> <span data-ttu-id="37c30-150">Dans le cas contraire, vous devez ignorer **lSampleSize**.</span><span class="sxs-lookup"><span data-stu-id="37c30-150">Otherwise, you should ignore **lSampleSize**.</span></span>
-   <span data-ttu-id="37c30-151">**bTemporalCompression**.</span><span class="sxs-lookup"><span data-stu-id="37c30-151">**bTemporalCompression**.</span></span> <span data-ttu-id="37c30-152">Si cet indicateur booléen a la **valeur false**, cela signifie que tous les frames sont des images clés.</span><span class="sxs-lookup"><span data-stu-id="37c30-152">If this Boolean flag is **FALSE**, it means that all frames are key frames.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37c30-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="37c30-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37c30-154">Le graphique de filtre et ses composants</span><span class="sxs-lookup"><span data-stu-id="37c30-154">The Filter Graph and Its Components</span></span>](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 
