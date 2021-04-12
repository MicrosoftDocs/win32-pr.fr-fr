---
description: Utilisation de demux avec des flux élémentaires
ms.assetid: dd98aada-8309-428e-9609-2542195bc6ec
title: Utilisation de demux avec des flux élémentaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6b9004d6c99db96405797016b0d9854c96dae92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319534"
---
# <a name="using-the-demux-with-elementary-streams"></a><span data-ttu-id="e3613-103">Utilisation de demux avec des flux élémentaires</span><span class="sxs-lookup"><span data-stu-id="e3613-103">Using the Demux with Elementary Streams</span></span>

<span data-ttu-id="e3613-104">Lorsque le demux MPEG-2 fournit des charges utiles PES, il envoie le flux ES octets dans des lots d’exemples de supports.</span><span class="sxs-lookup"><span data-stu-id="e3613-104">When the MPEG-2 demux delivers PES payloads, it sends the ES byte stream in batches of media samples.</span></span> <span data-ttu-id="e3613-105">La taille par défaut de l’échantillon est de 8 Ko.</span><span class="sxs-lookup"><span data-stu-id="e3613-105">The default sample size is 8K.</span></span> <span data-ttu-id="e3613-106">Le demux démarre un nouvel exemple de support sur chaque limite PES, mais peut décomposer une seule charge PES en plusieurs échantillons.</span><span class="sxs-lookup"><span data-stu-id="e3613-106">The demux starts a new media sample on each PES boundary, but may break a single PES payload into several samples.</span></span> <span data-ttu-id="e3613-107">Par exemple, si une charge utile PES est de 20 000, elle sera fournie dans deux échantillons de 8 Ko, suivis d’un échantillon de 4 Ko.</span><span class="sxs-lookup"><span data-stu-id="e3613-107">For example, if a PES payload is 20K, it will be delivered in two 8K samples followed by one 4K sample.</span></span> <span data-ttu-id="e3613-108">Demux n’examine pas le contenu du flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="e3613-108">The demux does not examine the contents of the byte stream.</span></span> <span data-ttu-id="e3613-109">Il revient au décodeur d’analyser les en-têtes de séquence et de rechercher les modifications de format.</span><span class="sxs-lookup"><span data-stu-id="e3613-109">It is up to the decoder to parse the sequence headers and look for format changes.</span></span>

<span data-ttu-id="e3613-110">Lorsque la broche de sortie du filtre demux se connecte au décodeur, elle offre le type de média qui a été spécifié lors de la création du code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="e3613-110">When the demux filter's output pin connects to the decoder, it offers the media type that was specified when the pin was created.</span></span> <span data-ttu-id="e3613-111">Étant donné que demux n’examine pas le flux de bits ES, il ne valide pas le type de média.</span><span class="sxs-lookup"><span data-stu-id="e3613-111">Because the demux does not examine the ES byte stream, it does not validate the media type.</span></span> <span data-ttu-id="e3613-112">En théorie, un décodeur MPEG-2 doit être en mesure de se connecter avec uniquement le type et le sous-type majeurs remplis, pour indiquer le type de données.</span><span class="sxs-lookup"><span data-stu-id="e3613-112">In theory, an MPEG-2 decoder should be able to connect with just the major type and subtype filled in, to indicate the type of data.</span></span> <span data-ttu-id="e3613-113">Le décodeur doit ensuite examiner les en-têtes de séquence qui arrivent dans les exemples de supports.</span><span class="sxs-lookup"><span data-stu-id="e3613-113">The decoder should then examine the sequence headers that arrive in the media samples.</span></span> <span data-ttu-id="e3613-114">Toutefois, dans la pratique, de nombreux décodeurs ne se connectent pas à moins que le type de média inclue un bloc de format complet.</span><span class="sxs-lookup"><span data-stu-id="e3613-114">However, in practice, many decoders will not connect unless the media type includes a complete format block.</span></span>

<span data-ttu-id="e3613-115">Par exemple, supposons que PID 0x31 contient la vidéo sur le profil principal MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="e3613-115">For example, suppose that PID 0x31 contains MPEG-2 main profile video.</span></span> <span data-ttu-id="e3613-116">Au minimum, vous devez effectuer les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="e3613-116">At a minimum, you would need to do the following steps.</span></span>

<span data-ttu-id="e3613-117">Tout d’abord, créez un type de média pour la vidéo MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="e3613-117">First, create a media type for MPEG-2 video.</span></span> <span data-ttu-id="e3613-118">Laisser le bloc de format pour le moment :</span><span class="sxs-lookup"><span data-stu-id="e3613-118">Leaving aside the format block for now:</span></span>


```C++
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
// Possibly create a format block (not shown here).
```



<span data-ttu-id="e3613-119">Ensuite, créez une broche de sortie sur le demux :</span><span class="sxs-lookup"><span data-stu-id="e3613-119">Next, create an output pin on the demux:</span></span>


```C++
// Query the demux filter for IMpeg2Demultiplexer.
IMpeg2Demultiplexer *pDemux;
hr = pFilter->QueryInterface(IID_IMpeg2Demultiplexer, (void**)&pDemux);
if (SUCCEEDED(hr))
{
    // Create a new output pin.
    IPin *pPin0;
    hr = pDemux->CreateOutputPin(&mt, L"Video Pin", &pPin0);
    if (SUCCEEDED(hr))
    {
        ....
    }
}
```



<span data-ttu-id="e3613-120">Interrogez ensuite le nouveau code PIN de l’interface **IMPEG2PIDMap** et appelez **MapPID**.</span><span class="sxs-lookup"><span data-stu-id="e3613-120">Then, query the new pin for the **IMPEG2PIDMap** interface and call **MapPID**.</span></span> <span data-ttu-id="e3613-121">Spécifiez PID Number 0x30 et MEDIA \_ élémentaire \_ Stream pour les charges utiles PES.</span><span class="sxs-lookup"><span data-stu-id="e3613-121">Specify PID number 0x30, and MEDIA\_ELEMENTARY\_STREAM for PES payloads.</span></span>


```C++
// Query the pin for IMPEG2PIDMap. This implicitly configures the
// demux to carry a transport stream. 
IMPEG2PIDMap *pPidMap;
hr = pPin0->QueryInterface(IID_IMPEG2PIDMap, (void**)&pPidMap);
if (SUCCEEDED(hr))
{
    // Assign PID 0x31 to pin 0. Set the type to "PES payload."
    ULONG Pid = 0x031;
    hr = pPidMap->MapPID(1, &Pid, MEDIA_ELEMENTARY_STREAM);
    pPidMap->Release();
}
```



<span data-ttu-id="e3613-122">Enfin, libérez toutes les interfaces quand vous avez terminé :</span><span class="sxs-lookup"><span data-stu-id="e3613-122">Finally, release all interfaces when you are done:</span></span>


```C++
pPin0->Release();
pDemux->Release();
```



<span data-ttu-id="e3613-123">Voici un exemple plus complet de définition du type de média, y compris le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="e3613-123">Here is a more complete example of setting the media type, including the format block.</span></span> <span data-ttu-id="e3613-124">Cet exemple suppose toujours une vidéo de profil principal MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="e3613-124">This example still assumes an MPEG-2 main profile video.</span></span> <span data-ttu-id="e3613-125">Les détails varient en fonction du contenu du flux :</span><span class="sxs-lookup"><span data-stu-id="e3613-125">The details will vary depending on stream contents:</span></span>


```C++
// Set up a byte array to hold the first sequence header. 
// This may or may not be required, depending on the decoder.
BYTE SeqHdr[] = { ... };  // Contains the sequence header (not shown).

AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
mt.formattype = FORMAT_MPEG2Video;

// Allocate the format block, including space for the sequence header. 
mt.cbFormat = sizeof(MPEG2VIDEOINFO) + sizeof(SeqHdr);
mt.pbFormat = (BYTE*)CoTaskMemAlloc(mt.cbFormat);
if (mt.pbFormat == NULL)
{
    // Out of memory; return an error code.
}
ZeroMemory(mt.pbFormat, mt.cbFormat);

// Cast the buffer pointer to an MPEG2VIDEOINFO struct.
MPEG2VIDEOINFO *pMVIH = (MPEG2VIDEOINFO*)mt.pbFormat;

RECT rcSrc = {0, 480, 0, 720};        // Source rectangle.
pMVIH->hdr.rcSource = rcSrc;
pMVIH->hdr.dwBitRate = 4000000;       // Bit rate.
pMVIH->hdr.AvgTimePerFrame = 333667;  // 29.97 fps.
pMVIH->hdr.dwPictAspectRatioX = 4;    // 4:3 aspect ratio.
pMVIH->hdr.dwPictAspectRatioY = 3;

// BITMAPINFOHEADER information.
pMVIH->hdr.bmiHeader.biSize = 40;
pMVIH->hdr.bmiHeader.biWidth = 720;
pMVIH->hdr.bmiHeader.biHeight = 480;

pMVIH->dwLevel = AM_MPEG2Profile_Main;  // MPEG-2 profile. 
pMVIH->dwProfile = AM_MPEG2Level_Main;  // MPEG-2 level.

// Copy the sequence header into the format block.
pMVIH->cbSequenceHeader = sizeof(SeqHdr); // Size of sequence header.
memcpy(pMVIH->dwSequenceHeader, SeqHdr, sizeof(SeqHdr));
```



## <a name="related-topics"></a><span data-ttu-id="e3613-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e3613-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3613-127">Utilisation du démultiplexeur MPEG-2</span><span class="sxs-lookup"><span data-stu-id="e3613-127">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



