---
description: Génération d’exemples de flux à partir d’un objet de données ASF existant
ms.assetid: eb27f122-d958-495d-98ea-8befd105a9a8
title: Génération d’exemples de flux à partir d’un objet de données ASF existant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee612c9352e3295d6b4957922e385de40a9a1fa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111767"
---
# <a name="generating-stream-samples-from-an-existing-asf-data-object"></a><span data-ttu-id="d3713-103">Génération d’exemples de flux à partir d’un objet de données ASF existant</span><span class="sxs-lookup"><span data-stu-id="d3713-103">Generating Stream Samples from an Existing ASF Data Object</span></span>

<span data-ttu-id="d3713-104">L’objet *séparateur* ASF est un composant de couche WMContainer qui analyse l’objet de données ASF d’un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="d3713-104">The ASF *splitter* object is a WMContainer layer component that parses the ASF Data Object of an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="d3713-105">Avant de passer des paquets de données au séparateur, l’application doit initialiser, configurer et sélectionner des flux sur le séparateur afin de le préparer pour le processus d’analyse.</span><span class="sxs-lookup"><span data-stu-id="d3713-105">Before passing data packets to the splitter, the application must initialize, configure, and select streams on the splitter in order to prepare it for the parsing process.</span></span> <span data-ttu-id="d3713-106">Pour plus d’informations, consultez [création de l’objet Splitter ASF](creating-the-asf-splitter-object.md) et [configuration de l’objet Splitter ASF](configuring-the-asf-splitter-object.md).</span><span class="sxs-lookup"><span data-stu-id="d3713-106">For information, see [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md) and [Configuring the ASF Splitter Object](configuring-the-asf-splitter-object.md).</span></span>

<span data-ttu-id="d3713-107">Les méthodes requises pour l’analyse de l’objet de données ASF sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d3713-107">The methods required for parsing the ASF Data Object are:</span></span>

-   <span data-ttu-id="d3713-108">[**IMFASFSplitter ::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) qui démarre le processus d’analyse en poussant le tampon contenant les paquets de données vers le séparateur.</span><span class="sxs-lookup"><span data-stu-id="d3713-108">[**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) that starts the parsing process by pushing the buffer containing data packets to the splitter.</span></span>
-   <span data-ttu-id="d3713-109">[**IMFASFSplitter :: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) qui collecte les exemples de flux générés à partir de la mémoire tampon transmise au séparateur.</span><span class="sxs-lookup"><span data-stu-id="d3713-109">[**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) that collects stream samples that were generated from the buffer passed to splitter.</span></span>

## <a name="finding-the-data-offset"></a><span data-ttu-id="d3713-110">Recherche du décalage des données</span><span class="sxs-lookup"><span data-stu-id="d3713-110">Finding the Data Offset</span></span>

<span data-ttu-id="d3713-111">Avant de commencer le processus d’analyse, l’application doit localiser l’objet de données dans le fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="d3713-111">Before starting the parsing process, the application must locate the Data Object within the ASF file.</span></span> <span data-ttu-id="d3713-112">Il existe deux façons d’afficher le décalage de l’objet de données à partir du début du fichier :</span><span class="sxs-lookup"><span data-stu-id="d3713-112">There are two ways to get the offset of the Data Object from the start of the file:</span></span>

-   <span data-ttu-id="d3713-113">Avant d’initialiser l’objet ContentInfo, vous pouvez appeler la méthode [**IMFASFContentInfo :: GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) .</span><span class="sxs-lookup"><span data-stu-id="d3713-113">Before you have initialized the ContentInfo object, you can call the [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) method.</span></span> <span data-ttu-id="d3713-114">Cette méthode requiert une mémoire tampon qui contient les 30 premiers octets de l’en-tête ASF.</span><span class="sxs-lookup"><span data-stu-id="d3713-114">This method requires a buffer that contains the first 30 bytes of the ASF header.</span></span> <span data-ttu-id="d3713-115">Elle retourne la taille de l’en-tête entier qui indique le décalage par rapport au premier paquet de données.</span><span class="sxs-lookup"><span data-stu-id="d3713-115">It returns the size of the entire header that indicates the offset to the first data packet.</span></span> <span data-ttu-id="d3713-116">Cette valeur comprend également la taille de l’en-tête de l’objet de données de 50 octets.</span><span class="sxs-lookup"><span data-stu-id="d3713-116">This value also includes the Data Object header size of 50 bytes.</span></span>
-   <span data-ttu-id="d3713-117">Une fois que vous avez initialisé l’objet ContentInfo, vous pouvez obtenir le descripteur de présentation en appelant [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor), puis en interrogeant le descripteur de présentation pour l’attribut de [**\_ décalage de \_ \_ \_ début \_ de données ASF pour MF PD**](mf-pd-asf-data-start-offset-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="d3713-117">After you have initialized the ContentInfo object, you can get the presentation descriptor by calling [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor), and then querying the presentation descriptor for the [**MF\_PD\_ASF\_DATA\_START\_OFFSET**](mf-pd-asf-data-start-offset-attribute.md) attribute.</span></span> <span data-ttu-id="d3713-118">La valeur de cet attribut correspond à la taille de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="d3713-118">The value of this attribute is the header size.</span></span>
    > [!Note]  
    > <span data-ttu-id="d3713-119">L’attribut de [**\_ \_ \_ \_ longueur de données ASF PD ASF**](mf-pd-asf-data-length-attribute.md) sur le descripteur de présentation spécifie la longueur de l’objet de données ASF.</span><span class="sxs-lookup"><span data-stu-id="d3713-119">The [**MF\_PD\_ASF\_DATA\_LENGTH**](mf-pd-asf-data-length-attribute.md) attribute on the presentation descriptor specifies the length of the ASF Data Object.</span></span>

     

<span data-ttu-id="d3713-120">Dans les deux cas, la valeur retournée est la taille de l’objet d’en-tête plus la taille de la section d’en-tête de l’objet de données.</span><span class="sxs-lookup"><span data-stu-id="d3713-120">In both cases, the returned value is the size of the Header Object plus the size of the header section of the Data Object.</span></span> <span data-ttu-id="d3713-121">Par conséquent, la valeur résultante est le décalage au début des paquets de données dans l’objet de données ASF.</span><span class="sxs-lookup"><span data-stu-id="d3713-121">Therefore, the resulting value is the offset to the start of the data packets in the ASF Data Object.</span></span> <span data-ttu-id="d3713-122">Lorsque vous commencez à envoyer des données au séparateur, les données doivent commencer à ce décalage à partir du début du fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="d3713-122">When you begin sending data to the splitter, the data must start at this offset from the beginning of the ASF file.</span></span>

<span data-ttu-id="d3713-123">La valeur de décalage est passée en tant que paramètre à **ParseData** qui démarre le processus d’analyse.</span><span class="sxs-lookup"><span data-stu-id="d3713-123">The offset value is passed as a parameter to **ParseData** that starts the parsing process.</span></span>

<span data-ttu-id="d3713-124">L’objet de données est divisé en paquets de données.</span><span class="sxs-lookup"><span data-stu-id="d3713-124">The Data Object is divided into data packets.</span></span> <span data-ttu-id="d3713-125">Chaque paquet de données contient un en-tête de paquet de données qui fournit des informations d’analyse de paquets et les données de charge utile, les données de support numérique réelles.</span><span class="sxs-lookup"><span data-stu-id="d3713-125">Each data packet contains a data packet header that provides packet parsing information and the payload data—the actual digital media data.</span></span> <span data-ttu-id="d3713-126">Dans un scénario de recherche, l’application peut souhaiter que le séparateur commence l’analyse au niveau d’un paquet de données particulier.</span><span class="sxs-lookup"><span data-stu-id="d3713-126">In a seeking scenario, the application might want the splitter to start parsing at a particular data packet.</span></span> <span data-ttu-id="d3713-127">Pour ce faire, vous pouvez utiliser l’indexeur ASF pour récupérer le décalage.</span><span class="sxs-lookup"><span data-stu-id="d3713-127">To do this, you can use the ASF Indexer is used to retrieve the offset.</span></span> <span data-ttu-id="d3713-128">L’indexeur retourne une valeur de décalage qui commence à la limite du paquet.</span><span class="sxs-lookup"><span data-stu-id="d3713-128">The indexer returns an offset value that starts at the packet boundary.</span></span> <span data-ttu-id="d3713-129">Si vous n’utilisez pas l’indexeur, assurez-vous que l’offset commence au début de l’en-tête de paquet de données.</span><span class="sxs-lookup"><span data-stu-id="d3713-129">If you are not using the indexer, make sure that the offset starts at the start of the data packet header.</span></span> <span data-ttu-id="d3713-130">Si un décalage non valide est passé au séparateur, par exemple si la valeur ne pointe pas vers la limite du paquet, les appels **ParseHeader** et **GetNextSample** réussissent mais **GetNextSample** ne récupère aucun échantillon et la **valeur null** est reçue dans le paramètre *pSample* .</span><span class="sxs-lookup"><span data-stu-id="d3713-130">If an invalid offset is passed to the splitter, such as the value does not point at the packet boundary, **ParseHeader** and **GetNextSample** calls succeed but **GetNextSample** does not retrieve any samples and **NULL** is received in the *pSample* parameter.</span></span>

<span data-ttu-id="d3713-131">Si le séparateur est configuré pour analyser dans le sens inverse, le séparateur commence toujours l’analyse à la fin de la mémoire tampon du média qui est transmise à **ParseData**.</span><span class="sxs-lookup"><span data-stu-id="d3713-131">If the splitter is configured to parse in the reverse direction, then the splitter always starts parsing at the end of the media buffer that is passed to **ParseData**.</span></span> <span data-ttu-id="d3713-132">Par conséquent, pour l’analyse inverse dans l’appel à **ParseData**, transmettez l’offset dans le paramètre *cbLength* , qui spécifie la longueur des données et définissez *cbBufferOffset* sur zéro.</span><span class="sxs-lookup"><span data-stu-id="d3713-132">Therefore, for reverse parsing in the call to **ParseData**, pass the offset in the *cbLength* parameter, which specifies the length of the data and set *cbBufferOffset* to zero.</span></span>

## <a name="generating-samples-for-asf-data-packets"></a><span data-ttu-id="d3713-133">Génération d’exemples pour les paquets de données ASF</span><span class="sxs-lookup"><span data-stu-id="d3713-133">Generating Samples for ASF Data Packets</span></span>

<span data-ttu-id="d3713-134">Une application démarre le processus d’analyse en passant les paquets de données au séparateur.</span><span class="sxs-lookup"><span data-stu-id="d3713-134">An application starts the parsing process by passing the data packets to the splitter.</span></span> <span data-ttu-id="d3713-135">L’entrée du séparateur est une série de mémoires tampons de média qui contiennent l’intégralité ou les fragments de l’objet de données.</span><span class="sxs-lookup"><span data-stu-id="d3713-135">The input to the splitter is a series of media buffers that contain the entire or fragments of the Data Object.</span></span> <span data-ttu-id="d3713-136">La sortie du séparateur est une série d’exemples de médias qui contiennent les données du paquet.</span><span class="sxs-lookup"><span data-stu-id="d3713-136">The output from the splitter is a series of media samples that contain the packet data.</span></span>

<span data-ttu-id="d3713-137">Pour transmettre des données d’entrée au séparateur, créez une mémoire tampon de média et remplissez-la avec les données de la section de l’objet de données du fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="d3713-137">To pass input data to the splitter, create a media buffer and fill it with data from the Data Object section of the ASF file.</span></span> <span data-ttu-id="d3713-138">(Pour plus d’informations sur les mémoires tampons de média, consultez [mémoires tampons de média](media-buffers.md).) Ensuite, transmettez la mémoire tampon du média à la méthode [**IMFASFSplitter ::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) .</span><span class="sxs-lookup"><span data-stu-id="d3713-138">(For more information about media buffers, see [Media Buffers](media-buffers.md).) Then, pass the media buffer to the [**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) method.</span></span> <span data-ttu-id="d3713-139">Vous pouvez également spécifier :</span><span class="sxs-lookup"><span data-stu-id="d3713-139">You can also specify:</span></span>

-   <span data-ttu-id="d3713-140">Offset dans la mémoire tampon où le séparateur doit commencer l’analyse.</span><span class="sxs-lookup"><span data-stu-id="d3713-140">The offset into the buffer where the splitter should start parsing.</span></span> <span data-ttu-id="d3713-141">Si le décalage est égal à zéro, l’analyse commence au début de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d3713-141">If the offset is zero, parsing begins at the start of the buffer.</span></span> <span data-ttu-id="d3713-142">Pour plus d’informations sur la définition du décalage des données, consultez la section « recherche de l’offset des données » dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="d3713-142">For information about setting the data offset, see the "Finding the Data Offset" section in this topic.</span></span>
-   <span data-ttu-id="d3713-143">Quantité de données à analyser.</span><span class="sxs-lookup"><span data-stu-id="d3713-143">The amount of data to parse.</span></span> <span data-ttu-id="d3713-144">Si cette valeur est égale à zéro, le séparateur est analysé jusqu’à ce qu’il atteigne la fin de la mémoire tampon, comme spécifié par la méthode [**IMFMediaBuffer :: GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) .</span><span class="sxs-lookup"><span data-stu-id="d3713-144">If this value is zero, the splitter parses until it reaches the end of the buffer, as specified by the [**IMFMediaBuffer::GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) method.</span></span>

<span data-ttu-id="d3713-145">Le séparateur génère des exemples de médias en référençant les données dans les mémoires tampons du média.</span><span class="sxs-lookup"><span data-stu-id="d3713-145">The splitter generates media samples by referencing the data in the media buffers.</span></span> <span data-ttu-id="d3713-146">Le client peut récupérer les exemples de sortie en appelant [**IMFASFSplitter :: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) dans une boucle jusqu’à ce qu’il n’y ait plus de données à analyser.</span><span class="sxs-lookup"><span data-stu-id="d3713-146">The client can retrieve the output samples by calling [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in a loop until there is no more data to parse.</span></span> <span data-ttu-id="d3713-147">Si **GetNextSample** retourne l' \_ indicateur ASF STATUSFLAGS \_ incomplet dans le paramètre *pdwStatusFlags* , cela signifie qu’il y a plus d’échantillons à récupérer, et que l’application peut appeler de nouveau **GetNextSample** .</span><span class="sxs-lookup"><span data-stu-id="d3713-147">If **GetNextSample** returns the ASF\_STATUSFLAGS\_INCOMPLETE flag in the *pdwStatusFlags* parameter, it means there are more samples to retrieve, and the application can call **GetNextSample** again.</span></span> <span data-ttu-id="d3713-148">Sinon, appelez **ParseData** pour transmettre plus de données au séparateur.</span><span class="sxs-lookup"><span data-stu-id="d3713-148">Otherwise, call **ParseData** to pass more data to the splitter.</span></span> <span data-ttu-id="d3713-149">Pour les exemples générés, le séparateur définit les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d3713-149">For the generated samples, the splitter sets the following information:</span></span>

-   <span data-ttu-id="d3713-150">Le séparateur définit un horodatage sur tous les exemples qu’il génère.</span><span class="sxs-lookup"><span data-stu-id="d3713-150">The splitter sets a time stamp on all the samples that it generates.</span></span> <span data-ttu-id="d3713-151">L’heure de l’exemple représente l’heure de présentation et n’inclut pas le temps de préroll.</span><span class="sxs-lookup"><span data-stu-id="d3713-151">The sample time represents the presentation time and does not include the preroll time.</span></span> <span data-ttu-id="d3713-152">L’application peut appeler [**IMFSample :: GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) pour connaître l’heure de présentation, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="d3713-152">The application can call [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) to get the presentation time, in 100-nanosecond units.</span></span>
-   <span data-ttu-id="d3713-153">Si une interruption se produit pendant la génération de l’échantillon, le séparateur définit l’attribut de [**\_ discontinuité MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) sur le premier échantillon après la discontinuation.</span><span class="sxs-lookup"><span data-stu-id="d3713-153">If a break occurs during sample generation, the splitter sets the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute on the first sample after the discontinuity.</span></span> <span data-ttu-id="d3713-154">Les discontinuités sont généralement dues à des paquets ignorés sur une connexion réseau, à des données de fichier endommagées ou à un déplacement de fractionnement d’un flux source à un autre.</span><span class="sxs-lookup"><span data-stu-id="d3713-154">Discontinuities are usually caused by dropped packets on a network connection, corrupt file data, or the splitter switching from one source stream to another.</span></span>
-   <span data-ttu-id="d3713-155">Pour la vidéo, le séparateur vérifie si l’échantillon contient une image clé.</span><span class="sxs-lookup"><span data-stu-id="d3713-155">For video, the splitter checks whether the sample contains a key frame.</span></span> <span data-ttu-id="d3713-156">Si c’est le cas, le séparateur définit l’attribut [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) sur l’exemple.</span><span class="sxs-lookup"><span data-stu-id="d3713-156">If it does, the splitter sets the [**MFSampleExtension\_CleanPoint**](mfsampleextension-cleanpoint-attribute.md) attribute on the sample.</span></span>

<span data-ttu-id="d3713-157">Si le séparateur analyse les paquets de données reçus d’un serveur multimédia, il est possible que la longueur du paquet soit variable.</span><span class="sxs-lookup"><span data-stu-id="d3713-157">If the splitter is parsing data packets that are received from a media server, it is possible that the packet length is variable.</span></span> <span data-ttu-id="d3713-158">Dans ce cas, le client doit appeler **ParseData** pour chaque paquet et définir l’attribut de [**\_ \_ limite de paquet MFASFSPLITTER**](mfasfsplitter-packet-boundary-attribute.md) sur chaque mémoire tampon qui est envoyée au séparateur.</span><span class="sxs-lookup"><span data-stu-id="d3713-158">In this case, the client must call **ParseData** for each packet and set the [**MFASFSPLITTER\_PACKET\_BOUNDARY**](mfasfsplitter-packet-boundary-attribute.md) attribute on each buffer that is sent to the splitter.</span></span> <span data-ttu-id="d3713-159">Cet attribut indique au séparateur si la mémoire tampon du média contient le début d’un paquet ASF.</span><span class="sxs-lookup"><span data-stu-id="d3713-159">This attribute indicates to the splitter whether the media buffer contains the start of an ASF packet.</span></span> <span data-ttu-id="d3713-160">Affectez la **valeur true** à l’attribut si la mémoire tampon contient le début d’un nouveau paquet.</span><span class="sxs-lookup"><span data-stu-id="d3713-160">Set the attribute to **TRUE** if the buffer contains the start of a new packet.</span></span> <span data-ttu-id="d3713-161">Si la mémoire tampon contient une continuation du paquet précédent, affectez la valeur **false** à l’attribut.</span><span class="sxs-lookup"><span data-stu-id="d3713-161">If the buffer contains a continuation of the previous packet, set the attribute to **FALSE**.</span></span> <span data-ttu-id="d3713-162">Les mémoires tampons ne peuvent pas couvrir plusieurs paquets.</span><span class="sxs-lookup"><span data-stu-id="d3713-162">The buffers cannot span multiple packets.</span></span>

<span data-ttu-id="d3713-163">Avant de passer de nouvelles mémoires tampons de média au séparateur, l’application doit appeler [**IMFASFSplitter :: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush).</span><span class="sxs-lookup"><span data-stu-id="d3713-163">Before passing new media buffers to the splitter, the application must call [**IMFASFSplitter::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush).</span></span> <span data-ttu-id="d3713-164">Cette méthode réinitialise le séparateur et efface tout Frame partiel en attente d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="d3713-164">This method resets the splitter and clears any partial frame that is waiting to be completed.</span></span> <span data-ttu-id="d3713-165">Cela est utile dans un scénario de recherche où le décalage se trouve à un emplacement différent.</span><span class="sxs-lookup"><span data-stu-id="d3713-165">This is useful in a seeking scenario where the offset is at a different location.</span></span>

### <a name="example"></a><span data-ttu-id="d3713-166">Exemple</span><span class="sxs-lookup"><span data-stu-id="d3713-166">Example</span></span>

<span data-ttu-id="d3713-167">L’exemple de code suivant montre comment analyser des paquets de données.</span><span class="sxs-lookup"><span data-stu-id="d3713-167">The following code example shows how to parse data packets.</span></span> <span data-ttu-id="d3713-168">Cet exemple analyse à partir du début de l’objet de données jusqu’à la fin du flux et affiche des informations sur les exemples qui contiennent des images clés.</span><span class="sxs-lookup"><span data-stu-id="d3713-168">This example parses from the beginning of the Data Object to the end of the stream and displays information about the samples that contain key frames.</span></span> <span data-ttu-id="d3713-169">Pour obtenir un exemple complet qui utilise ce code, consultez [Didacticiel : lecture d’un fichier ASF](tutorial--reading-an-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="d3713-169">For a complete example that uses this code, see [Tutorial: Reading an ASF File](tutorial--reading-an-asf-file.md).</span></span>


```C++
// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d3713-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3713-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3713-171">Séparateur ASF</span><span class="sxs-lookup"><span data-stu-id="d3713-171">ASF Splitter</span></span>](asf-splitter.md)
</dt> </dl>

 

 



