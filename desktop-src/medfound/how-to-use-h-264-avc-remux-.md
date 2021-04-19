---
description: Cette rubrique décrit quand et comment utiliser un récepteur MFT et MP4 REMUX H. 264/AVC.
ms.assetid: 1DD236D9-775B-4417-BC49-BF52A6B3C8AD
title: Quand et comment utiliser H. 264/AVC REMUX MFT et le récepteur MP4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132c582fa16eae56c4fec8809caa4bd501469e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106541203"
---
# <a name="when-and-how-to-use-h264avc-remux-mft-and-mp4-sink"></a><span data-ttu-id="1b166-103">Quand et comment utiliser H. 264/AVC REMUX MFT et le récepteur MP4</span><span class="sxs-lookup"><span data-stu-id="1b166-103">When and How to Use H.264/AVC Remux MFT and MP4 Sink</span></span>

<span data-ttu-id="1b166-104">Cette rubrique décrit quand et comment utiliser un récepteur MFT et MP4 REMUX H. 264/AVC.</span><span class="sxs-lookup"><span data-stu-id="1b166-104">This topic describes when and how to use a H.264/AVC Remux MFT and MP4 Sink.</span></span>

## <a name="when-to-use-h264avc-remux-mft"></a><span data-ttu-id="1b166-105">Quand utiliser H. 264/AVC REMUX MFT</span><span class="sxs-lookup"><span data-stu-id="1b166-105">When to use H.264/AVC Remux MFT</span></span>

<span data-ttu-id="1b166-106">Le format de fichier MPEG-4 requiert que chaque exemple compressé contienne une image principale avec des unités NAL dans le bon ordre.</span><span class="sxs-lookup"><span data-stu-id="1b166-106">MPEG-4 file format requires that each compressed sample contains one primary picture with NAL units in the correct order.</span></span> <span data-ttu-id="1b166-107">(Reportez-vous à la définition de l’image principale et à l’ordre des unités NAL obligatoires dans la section 7.4.1.2.3, **ordre des unités nal et des images codées et Association aux unités d’accès**, de la spécification AVC H. 264.) Elle requiert également que chaque exemple compressé soit associé à un horodatage de présentation, un horodatage de décodage et une durée d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="1b166-107">(Please refer to the definition of primary picture and mandatory NAL units order in section 7.4.1.2.3, **Order of NAL units and coded pictures and association to access units**, of the H.264 AVC specification.) It also requires each compressed sample is associated with a presentation time stamp, decoding time stamp, and sample duration.</span></span>

<span data-ttu-id="1b166-108">Dans de nombreux scénarios, lorsque les applications doivent enregistrer la vidéo H. 264/AVC dans un conteneur de fichiers MPEG-4, l’exemple compressé peut ne pas répondre aux exigences ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="1b166-108">In many scenarios when applications need to record H.264/AVC video in a MPEG-4 file container, the compressed sample may not satisfy the above requirements.</span></span> <span data-ttu-id="1b166-109">Par exemple, il se peut qu’un exemple compressé ne contienne pas d’image principale complète ou qu’il ne soit pas associé à un horodatage de présentation correct.</span><span class="sxs-lookup"><span data-stu-id="1b166-109">For example, one compressed sample might not contain a complete primary picture or might not have a correct presentation time stamp associated with it.</span></span> <span data-ttu-id="1b166-110">Voici quelques exemples d’applications :</span><span class="sxs-lookup"><span data-stu-id="1b166-110">A few application examples are:</span></span>

-   <span data-ttu-id="1b166-111">Écrire une vidéo élémentaire de streaming H. 264/AVC dans un conteneur de fichiers MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="1b166-111">Write H.264/AVC streaming elementary video into MPEG-4 file container.</span></span>
-   <span data-ttu-id="1b166-112">Enregistrement caméra capture d’une vidéo élémentaire H. 264/AVC dans le conteneur de fichiers MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="1b166-112">Record camera captured H.264/AVC elementary video in MPEG-4 file container.</span></span>
-   <span data-ttu-id="1b166-113">Enregistrez la conférence vidéo H. 264/AVC dans le conteneur de fichiers MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="1b166-113">Record H.264/AVC video conference in MPEG-4 file container.</span></span>
-   <span data-ttu-id="1b166-114">Concaténez deux vidéos H. 264/AVC dans MPEG-2 TS ou MP4 et écrivez dans le conteneur de fichiers MPEG-4 avec des horodatages corrects.</span><span class="sxs-lookup"><span data-stu-id="1b166-114">Concatenate two H.264/AVC video in MPEG-2 TS or MP4 and write into MPEG-4 file container with correct time stamps.</span></span>
-   <span data-ttu-id="1b166-115">Vidéo REMUX H. 264/AVC à partir du format de fichier AVCHD, MPEG-2 TS/PS au format de fichier MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="1b166-115">Remux H.264/AVC video from AVCHD, MPEG-2 TS/PS file format to MPEG-4 file format.</span></span>
-   <span data-ttu-id="1b166-116">Découpez le fichier vidéo H. 264/AVC sans transcodage.</span><span class="sxs-lookup"><span data-stu-id="1b166-116">Trim H.264/AVC video file without transcoding.</span></span>

<span data-ttu-id="1b166-117">Dans ce cas, l’application doit utiliser une table MFT REMUX H. 264/AVC pour convertir les exemples compressés qui ne contiennent pas d’image principale complète avant qu’ils ne soient écrits dans le conteneur de fichiers MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="1b166-117">In this situation, the application needs to use a H.264/AVC remux MFT to convert the compressed samples not containing a complete primary picture before they are written into the MPEG-4 file container.</span></span>

## <a name="how-to-use-h264avc-remux-mft-and-mp4-sink"></a><span data-ttu-id="1b166-118">Comment utiliser H. 264/AVC REMUX MFT et le récepteur MP4</span><span class="sxs-lookup"><span data-stu-id="1b166-118">How to use H.264/AVC Remux MFT and MP4 sink</span></span>

<span data-ttu-id="1b166-119">Définissez le type de média de sortie source sur **MFVideoFormat \_ H264 – \_ es**, ce qui indique que chaque exemple ne peut pas contenir une image principale complète.</span><span class="sxs-lookup"><span data-stu-id="1b166-119">Set the source output media type to **MFVideoFormat\_H264\_ES**, which indicates each sample might not contain a complete primary picture.</span></span> <span data-ttu-id="1b166-120">Définissez le type de média d’entrée du récepteur MP4 sur **MFVideoFormat \_ H264 –**.</span><span class="sxs-lookup"><span data-stu-id="1b166-120">Set the input media type of MP4 sink to **MFVideoFormat\_H264**.</span></span> <span data-ttu-id="1b166-121">Par conséquent, le type de média d’entrée de la MFT H. 264/AVC REMUX est **MFVideoFormat \_ H264 – \_ es** et le type de support de sortie de la MFT h. 264/AVC REMUX est **MFVideoFormat \_ H264 –**, qui sera automatiquement inséré dans le programme de résolution de topologie.</span><span class="sxs-lookup"><span data-stu-id="1b166-121">So, the input media type of the H.264/AVC remux MFT is **MFVideoFormat\_H264\_ES** and the output media type of the H.264/AVC remux MFT is **MFVideoFormat\_H264**, which will be automatically inserted into the topology resolver.</span></span>

<span data-ttu-id="1b166-122">La durée de l’échantillon est ignorée par le H. 264/AVC REMUX, car la durée de l’échantillon pour un exemple ne contenant pas d’image principale complète n’a pas de signification claire.</span><span class="sxs-lookup"><span data-stu-id="1b166-122">Sample duration is ignored by the H.264/AVC remux, because the sample duration for a sample not containing a complete primary picture does not have clear meaning.</span></span> <span data-ttu-id="1b166-123">Au lieu de cela, la durée de l’échantillon est calculée à partir de la fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="1b166-123">Instead, the sample duration is calculated from the frame rate.</span></span> <span data-ttu-id="1b166-124">La fréquence d’images est calculée à partir du paramètre Sequence.</span><span class="sxs-lookup"><span data-stu-id="1b166-124">The frame rate is calculated from the sequence parameter.</span></span> <span data-ttu-id="1b166-125">Si les informations n’existent pas dans le paramètre Sequence, la fréquence d’images est calculée à partir des paramètres du type de média d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1b166-125">If the information does not exist in the sequence parameter, the frame rate is calculated from the parameters in the input media type.</span></span> <span data-ttu-id="1b166-126">Si les informations de fréquence d’images ne sont pas disponibles, la fréquence d’images par défaut de 29,97 fps est utilisée.</span><span class="sxs-lookup"><span data-stu-id="1b166-126">If frame rate information is not available, the default frame rate of 29.97 fps is used.</span></span>

<span data-ttu-id="1b166-127">H. 264/AVC REMUX MFT interpole de manière linéaire les horodatages de décodage pour chaque image compressée en fonction de la fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="1b166-127">H.264/AVC remux MFT linearly interpolates the decoding time stamps (DTS) for each compressed picture according to the frame rate.</span></span> <span data-ttu-id="1b166-128">H. 264/AVC REMUX MFT honore les horodatages de présentation d’entrée (PTS) dans les exemples d’entrée et les transmet à la sortie s’ils existent.</span><span class="sxs-lookup"><span data-stu-id="1b166-128">H.264/AVC remux MFT honors the input presentation time stamps (PTS) in input samples and passes them to the output if they exist.</span></span> <span data-ttu-id="1b166-129">Il effectue une interpolation PTS en fonction de la fréquence d’images, de la PTS précédente et de l’ordre de sortie des images par le biais du processus de mise en mémoire tampon des images décodées (DBP), comme indiqué dans **l’annexe C.** point de vue du détourage de la spécification AVC H. 264.</span><span class="sxs-lookup"><span data-stu-id="1b166-129">It performs PTS interpolation according to frame rate, the previous PTS, and the picture output order through Decoded Picture Buffering (DBP) bumping process as specified in **Annex C.4.5.3 Bumping process** of the H.264 AVC specification.</span></span> <span data-ttu-id="1b166-130">Chaque échantillon de sortie de la MFT H. 264/AVC REMUX doit avoir des PTS, DTS et Sample Duration.</span><span class="sxs-lookup"><span data-stu-id="1b166-130">Each output sample from the H.264/AVC remux MFT shall have PTS, DTS, and sample duration.</span></span> <span data-ttu-id="1b166-131">H. 264/AVC REMUX MFT identifie également les images de m dans le flux binaire et les définit comme point de nettoyage avec l’attribut MF de [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="1b166-131">H.264/AVC remux MFT also identifies the IDR pictures in the bitstream and sets them as clean point with the MF attribute of [MFSampleExtension\_CleanPoint](mfsampleextension-cleanpoint-attribute.md).</span></span>

<span data-ttu-id="1b166-132">Actuellement, la MFT H. 264/AVC REMUX peut gérer un maximum de 64 frame de réorganisation.</span><span class="sxs-lookup"><span data-stu-id="1b166-132">Currently the H.264/AVC remux MFT can handle a maximum of 64 reordered frame.</span></span> <span data-ttu-id="1b166-133">Si le nombre de frames réorganisés dépasse 64 avec un cadre de référence à long terme, la MFT H. 264/AVC REMUX effectue l’interpolation d’une PTS erronée pour ce frame et génère cette trame à un moment incorrect.</span><span class="sxs-lookup"><span data-stu-id="1b166-133">If the number of reordered frame exceeds 64 with a long term reference frame present, the H.264/AVC remux MFT will interpolate a wrong PTS for that frame and output that frame at a wrong time.</span></span>

<span data-ttu-id="1b166-134">Pour instancier une table MFT REMUX H. 264/AVC, définissez les types de médias d’entrée et de sortie corrects sur la MFT H. 264/AVC REMUX, définissez le type de média d’entrée pour le récepteur MP4 et résolvez la topologie.</span><span class="sxs-lookup"><span data-stu-id="1b166-134">To instantiate a H.264/AVC remux MFT, set the correct input and output media types on the H.264/AVC remux MFT, set the input media type for the MP4 sink, and resolve the topology.</span></span>

<span data-ttu-id="1b166-135">L’exemple de code suivant montre comment initialiser le récepteur MFT. 264/AVC REMUX.</span><span class="sxs-lookup"><span data-stu-id="1b166-135">The following sample code show how to initialize the H.264/AVC remux MFT and MP4 sink.</span></span>

<span data-ttu-id="1b166-136">Pour la MFT H. 264/AVC REMUX,</span><span class="sxs-lookup"><span data-stu-id="1b166-136">For H.264/AVC remux MFT,</span></span>


```C++
hr = CoCreateInstance(
            CLSID_CMSH264RemuxMFT,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IMFTransform,
            (void**) &pIMFTransform
            );
```



<span data-ttu-id="1b166-137">Aucune autre configuration n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1b166-137">No further configuration is necessary.</span></span>

<span data-ttu-id="1b166-138">Pour le récepteur MP4,</span><span class="sxs-lookup"><span data-stu-id="1b166-138">For MP4 sink,</span></span>


```C++
IMFByteStream*  pMFBSOutputFile = NULL;
hr = MFCreateFile(
    MF_ACCESSMODE_READWRITE,
    MF_OPENMODE_DELETE_IF_EXIST,
    MF_FILEFLAGS_NONE,
    m_pszOutputFile,
    &pMFBSOutputFile);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create output file for MP4 Sink (hr=0x%x)", hr);
    break;
}

hr = MFCreateMPEG4MediaSink(
    pMFBSOutputFile,
    (guidMajorType == MFMediaType_Video) ? pMediaType : NULL,  // pMediaType comes from the output type of the remux MFT
    (guidMajorType == MFMediaType_Audio) ? pMediaType : NULL,
    &m_pMediaSink);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create MP4 Sink (hr=0x%x)", hr);
    break;
}
hr = m_pMediaSink->GetStreamSinkByIndex(0, &pStream);
```



## <a name="related-topics"></a><span data-ttu-id="1b166-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1b166-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b166-140">Formats multimédias pris en charge dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1b166-140">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



