---
description: Exemple de filtre de l’analyseur PSI
ms.assetid: e815d57f-25e5-4a71-8f40-e7abec0db236
title: Exemple de filtre de l’analyseur PSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1099375d2dbabf9ee6c8e891b0a1780bebbb599d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104560034"
---
# <a name="psi-parser-filter-sample"></a><span data-ttu-id="3f9df-103">Exemple de filtre de l’analyseur PSI</span><span class="sxs-lookup"><span data-stu-id="3f9df-103">PSI Parser Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="3f9df-104">Description</span><span class="sxs-lookup"><span data-stu-id="3f9df-104">Description</span></span>

<span data-ttu-id="3f9df-105">Le filtre de l’analyseur PSI reçoit des informations spécifiques au programme (PSI) à partir d’un flux de transport MPEG-2 et extrait les informations de programme de la table d’association de programmes (PAT) et des tables de cartes de programme (VPM).</span><span class="sxs-lookup"><span data-stu-id="3f9df-105">The PSI Parser filter receives Program Specific Information (PSI) from an MPEG-2 transport stream and extracts program information from the Program Association Table (PAT) and Program Map Tables (PMT).</span></span> <span data-ttu-id="3f9df-106">Ces informations permettent à une application de configurer le démultiplexeur MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="3f9df-106">This information enables an application to configure the MPEG-2 Demultiplexer.</span></span> <span data-ttu-id="3f9df-107">Le filtre prend en charge une interface personnalisée, [**IMpeg2PsiParser**](impeg2psiparser.md), pour récupérer les informations psi.</span><span class="sxs-lookup"><span data-stu-id="3f9df-107">The filter supports a custom interface, [**IMpeg2PsiParser**](impeg2psiparser.md), for retrieving the PSI information.</span></span>

<span data-ttu-id="3f9df-108">Ce filtre est conçu pour les appareils MPEG-2, tels que les caméscopes IEEE 1394 MPEG-2 et les appareils D-VHS.</span><span class="sxs-lookup"><span data-stu-id="3f9df-108">This filter is designed for MPEG-2 devices, such as IEEE 1394 MPEG-2 camcorders and D-VHS devices.</span></span> <span data-ttu-id="3f9df-109">Pour plus d’informations, consultez [pilote MSTape](mstape-driver.md) .</span><span class="sxs-lookup"><span data-stu-id="3f9df-109">See [MSTape Driver](mstape-driver.md) for more information.</span></span> <span data-ttu-id="3f9df-110">Les sources de diffusion de télévision numérique doivent utiliser un filtre TIF pour obtenir des informations sur le programme.</span><span class="sxs-lookup"><span data-stu-id="3f9df-110">Digital television broadcast sources should use a TIF filter to get program information.</span></span>

## <a name="usage"></a><span data-ttu-id="3f9df-111">Utilisation</span><span class="sxs-lookup"><span data-stu-id="3f9df-111">Usage</span></span>

<span data-ttu-id="3f9df-112">Vous pouvez tester le filtre de l’analyseur PSI dans GraphEdit comme suit :</span><span class="sxs-lookup"><span data-stu-id="3f9df-112">You can test the PSI Parser filter in GraphEdit as follows:</span></span>

1.  <span data-ttu-id="3f9df-113">Lancez GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="3f9df-113">Launch GraphEdit.</span></span>
2.  <span data-ttu-id="3f9df-114">Insérez une source de transport MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="3f9df-114">Insert an MPEG-2 transport source.</span></span> <span data-ttu-id="3f9df-115">Les caméscopes MPEG-2 et les appareils D-VHS apparaissent en tant que « périphérique de sous-unité de bande Microsoft AV/C » dans la catégorie sources de capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="3f9df-115">MPEG-2 camcorders and D-VHS devices appear as "Microsoft AV/C Tape Subunit Device" in the Video Capture Sources category.</span></span>
3.  <span data-ttu-id="3f9df-116">Connectez le filtre source au filtre de démultiplexage MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="3f9df-116">Connect the source filter to the MPEG-2 Demultiplexer filter.</span></span>
4.  <span data-ttu-id="3f9df-117">Utilisez la page de propriétés de demux pour créer une broche de sortie avec un type de média « PSI MPEG-2 PSI ».</span><span class="sxs-lookup"><span data-stu-id="3f9df-117">Use the property page on the demux to create an output pin with an "MPEG-2 PSI" media type.</span></span> <span data-ttu-id="3f9df-118">Ce code PIN propose les sections PAT et VPM.</span><span class="sxs-lookup"><span data-stu-id="3f9df-118">This pin will deliver the PAT and PMT sections.</span></span>
5.  <span data-ttu-id="3f9df-119">Utilisez la page de propriétés demux pour mapper PID 0x00 à la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="3f9df-119">Use the demux property page to map PID 0x00 to the output pin.</span></span> <span data-ttu-id="3f9df-120">Définissez le type de contenu sur « sections PSI PSI ».</span><span class="sxs-lookup"><span data-stu-id="3f9df-120">Set the content type to "MPEG2 PSI Sections".</span></span>
6.  <span data-ttu-id="3f9df-121">Connectez la broche de sortie demux à l’analyseur PSI, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="3f9df-121">Connect the demux output pin to PSI Parser, as shown in the following diagram.</span></span>

    ![graphique de filtre de l’analyseur psi](images/psi-parser.png)

7.  <span data-ttu-id="3f9df-123">Exécutez le graphique afin d’alimenter les données PSI vers le filtre de l’analyseur PSI.</span><span class="sxs-lookup"><span data-stu-id="3f9df-123">Run the graph, in order to feed PSI data to the PSI Parser filter.</span></span> <span data-ttu-id="3f9df-124">Au fur et à mesure que le filtre décode les sections PAT, il mappe automatiquement les pid PMT à la même broche de sortie sur le demux, afin qu’il reçoive les sections VPM.</span><span class="sxs-lookup"><span data-stu-id="3f9df-124">As the filter decodes the PAT sections, it automatically maps the PMT PIDs to the same output pin on the demux, so that it receives the PMT sections.</span></span>
8.  <span data-ttu-id="3f9df-125">Utilisez la page de propriétés de l’analyseur PSI pour sélectionner un numéro de programme.</span><span class="sxs-lookup"><span data-stu-id="3f9df-125">Use the PSI Parser property page to select a program number.</span></span> <span data-ttu-id="3f9df-126">La liste de flux élémentaires de la page de propriétés indique le PID et le type de flux associés à chaque flux élémentaire dans le programme sélectionné.</span><span class="sxs-lookup"><span data-stu-id="3f9df-126">The elementary stream list in the property page will show the PID and stream type associated with each elementary stream in the selected program.</span></span> <span data-ttu-id="3f9df-127">La page de propriétés est conçue pour reconnaître les types de flux définis dans la norme ISO/IEC 13818-1.</span><span class="sxs-lookup"><span data-stu-id="3f9df-127">The property page is designed to recognize stream types defined in ISO/IEC 13818-1.</span></span>
9.  <span data-ttu-id="3f9df-128">Entrez le numéro PID Audio dans la zone d’édition des **PID Audio** et le numéro PID de la vidéo dans la zone d’édition de la **vidéo PID** .</span><span class="sxs-lookup"><span data-stu-id="3f9df-128">Enter the audio PID number in the **Audio PID** edit box, and the video PID number in the **Video PID** edit box.</span></span>
10. <span data-ttu-id="3f9df-129">Cliquez sur le bouton **afficher le programme** .</span><span class="sxs-lookup"><span data-stu-id="3f9df-129">Click the **View Program** button.</span></span> <span data-ttu-id="3f9df-130">L’analyseur PSI configure les broches de sortie sur le demux pour qu’elles correspondent aux informations de flux de programme et restitue les codes confidentiels.</span><span class="sxs-lookup"><span data-stu-id="3f9df-130">The PSI Parser will configure the output pins on the demux to match the program stream information and render the pins.</span></span>

> [!Note]  
> <span data-ttu-id="3f9df-131">La page de propriétés de l’analyseur PSI est fournie pour faciliter le test et pour fournir un exemple de code qui configure le démultiplexeur MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="3f9df-131">The PSI Parser property page is provided to make testing easier, and to provide sample code that configures the MPEG-2 Demultiplexer.</span></span> <span data-ttu-id="3f9df-132">Elle n’est pas recommandée pour les applications.</span><span class="sxs-lookup"><span data-stu-id="3f9df-132">It is not recommended for applications to use.</span></span> <span data-ttu-id="3f9df-133">Les applications doivent configurer demux par programme.</span><span class="sxs-lookup"><span data-stu-id="3f9df-133">Applications should configure the demux programmatically.</span></span>

 

<span data-ttu-id="3f9df-134">Pour utiliser le filtre de l’analyseur PSI dans une application, commencez par créer le graphique de filtre de la source MPEG-2 sur le demux MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="3f9df-134">To use the PSI Parser filter in an application, start by building the filter graph from the MPEG-2 source to the MPEG-2 demux.</span></span> <span data-ttu-id="3f9df-135">Le code pour cette étape n’est pas indiqué ici, car la configuration exacte du graphique dépend de la source.</span><span class="sxs-lookup"><span data-stu-id="3f9df-135">Code for this step is not shown here, because the exact graph configuration will depend on the source.</span></span>

<span data-ttu-id="3f9df-136">Ensuite, créez une broche de sortie sur le demux pour les données PSI.</span><span class="sxs-lookup"><span data-stu-id="3f9df-136">Next, create an output pin on the demux for the PSI data.</span></span> <span data-ttu-id="3f9df-137">Mappez le PID 0x00, qui est réservé aux sections PAT, à ce code PIN, comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="3f9df-137">Map PID 0x00, which is reserved for PAT sections, to this pin, as shown in the following code:</span></span>


```C++
// Set the media type to MPEG-2 table sections.
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = KSDATAFORMAT_TYPE_MPEG2_SECTIONS;

// Create the pin.
IPin *pPsiPin;
hr = pDemux->CreateOutputPin(&mt, L"PSI", &pPsiPin);
if (SUCCEEDED(hr))
{
    // Map to PID 0.
    ULONG Pid = 0x00;
    hr = pPid->MapPID(1, &Pid, MEDIA_MPEG2_PSI);
}
```



<span data-ttu-id="3f9df-138">Pour plus d’informations, consultez [utilisation du démultiplexeur MPEG-2](using-the-mpeg-2-demultiplexer.md).</span><span class="sxs-lookup"><span data-stu-id="3f9df-138">For more information, see [Using the MPEG-2 Demultiplexer](using-the-mpeg-2-demultiplexer.md).</span></span>

<span data-ttu-id="3f9df-139">Ajoutez le filtre de l’analyseur PSI au graphique et connectez-le à la broche de sortie sur le demux.</span><span class="sxs-lookup"><span data-stu-id="3f9df-139">Add the PSI Parser filter to the graph and connect it to the output pin on the demux.</span></span> <span data-ttu-id="3f9df-140">Interrogez l’analyseur PSI pour l’interface [**IMpeg2PsiParser**](impeg2psiparser.md) .</span><span class="sxs-lookup"><span data-stu-id="3f9df-140">Query the PSI Parser for the [**IMpeg2PsiParser**](impeg2psiparser.md) interface.</span></span> <span data-ttu-id="3f9df-141">Exécutez maintenant le graphique et attendez les \_ événements de changement de programme EC \_ qui signalent une nouvelle section Pat ou VPM.</span><span class="sxs-lookup"><span data-stu-id="3f9df-141">Now run the graph and wait for EC\_PROGRAM\_CHANGED events, which signal a new PAT or PMT section.</span></span> <span data-ttu-id="3f9df-142">Cet événement est un événement personnalisé défini par le filtre de l’analyseur PSI.</span><span class="sxs-lookup"><span data-stu-id="3f9df-142">This event is a custom event defined by the PSI Parser filter.</span></span> <span data-ttu-id="3f9df-143">Lorsque vous recevez un \_ événement de changement de programme EC \_ , vous pouvez obtenir les informations PSI disponibles en appelant les méthodes **IMpeg2PsiParser** .</span><span class="sxs-lookup"><span data-stu-id="3f9df-143">When you receive an EC\_PROGRAM\_CHANGED event, you can get the available PSI information by calling **IMpeg2PsiParser** methods.</span></span> <span data-ttu-id="3f9df-144">Cette section décrit les méthodes dont vous aurez besoin le plus souvent.</span><span class="sxs-lookup"><span data-stu-id="3f9df-144">This section describes the methods you will need most often.</span></span>

<span data-ttu-id="3f9df-145">Pour connaître le nombre de programmes, utilisez la méthode [**IMpeg2PsiParser :: GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md) :</span><span class="sxs-lookup"><span data-stu-id="3f9df-145">To get the number of programs, use the [**IMpeg2PsiParser::GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md) method:</span></span>


```C++
int NumProgs = 0;
hr = pPsi->GetCountOfPrograms(&NumProgs);
```



<span data-ttu-id="3f9df-146">Pour obtenir le numéro de programme d’un programme spécifique, utilisez la méthode [**IMpeg2PsiParser :: GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md) :</span><span class="sxs-lookup"><span data-stu-id="3f9df-146">To get the program number for a specific program, use the [**IMpeg2PsiParser::GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md) method:</span></span>


```C++
WORD ProgNum = 0;
for (int i = 0; i < NumProgs; i++)
{
    hr = pPsi->GetRecordProgramNumber(i, &ProgNum);
    ...
}
```



<span data-ttu-id="3f9df-147">Le numéro de programme est utilisé pour obtenir les entrées VPM pour des programmes individuels.</span><span class="sxs-lookup"><span data-stu-id="3f9df-147">The program number is used to obtain the PMT entries for individual programs.</span></span> <span data-ttu-id="3f9df-148">Pour obtenir le nombre de flux élémentaires dans un programme, utilisez la méthode [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) :</span><span class="sxs-lookup"><span data-stu-id="3f9df-148">To get the number of elementary streams in a program, use the [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) method:</span></span>


```C++
WORD cElemStreams = 0;
hr = pPsi->GetCountOfElementaryStreams(ProgNum, &cElemStreams);
```



<span data-ttu-id="3f9df-149">Pour chaque flux élémentaire, la méthode [**IMpeg2PsiParser :: GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) retourne le PID, et la méthode [**IMpeg2PsiParser :: GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) retourne le type de flux :</span><span class="sxs-lookup"><span data-stu-id="3f9df-149">For each elementary stream, the [**IMpeg2PsiParser::GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) method returns the PID, and the [**IMpeg2PsiParser::GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) method returns the stream type:</span></span>


```C++
BYTE ESType = 0;
WORD ESPid = 0;
for (WORD j = 0; j < cElemStreams; j++)
{
    hr = pPsi->GetRecordElementaryPid(ProgNum, j, &ESPid);
    hr = pPsi->GetRecordStreamType(ProgNum, j, &ESType);
}
```



<span data-ttu-id="3f9df-150">Le PID et le type de flux vous permettent de configurer de nouvelles broches de sortie sur le démultiplexeur MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="3f9df-150">The PID and the stream type enable you to configure new output pins on the MPEG-2 Demultiplexer.</span></span> <span data-ttu-id="3f9df-151">Cela peut nécessiter une connaissance de la source d’origine.</span><span class="sxs-lookup"><span data-stu-id="3f9df-151">This may require some knowledge of the original source.</span></span> <span data-ttu-id="3f9df-152">Par exemple, la norme ISO/IEC 13818-1 définit les types de flux 0x80 à 0xFF comme « Private User », mais d’autres normes basées sur MPEG-2 peuvent attribuer d’autres significations à ces types.</span><span class="sxs-lookup"><span data-stu-id="3f9df-152">For example, ISO/IEC 13818-1 defines stream types 0x80 through 0xFF as "user private," but other standards that are based on MPEG-2 may assign other meanings to these types.</span></span>

<span data-ttu-id="3f9df-153">Le démultiplexeur MPEG-2 peut créer des codes confidentiels et de nouveaux mappages PID lorsque le graphique est en cours d’exécution, mais vous devez arrêter le graphique pour connecter les broches.</span><span class="sxs-lookup"><span data-stu-id="3f9df-153">The MPEG-2 Demultiplexer can create new pins and new PID mappings while the graph is running, but you must stop the graph to connect pins.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="3f9df-154">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="3f9df-154">Downloading the Sample</span></span>

<span data-ttu-id="3f9df-155">Pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3f9df-155">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="3f9df-156">Cet exemple est installé sous le chemin d’accès suivant : exemples *\[ racine \] du kit de développement logiciel (SDK)* \\ fichiers de \\ \\ \\ filtres DirectShow \\ PSIParser.</span><span class="sxs-lookup"><span data-stu-id="3f9df-156">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\PSIParser.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f9df-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3f9df-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f9df-158">Exemples DirectShow</span><span class="sxs-lookup"><span data-stu-id="3f9df-158">DirectShow Samples</span></span>](directshow-samples.md)
</dt> <dt>

[<span data-ttu-id="3f9df-159">**Interface IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="3f9df-159">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> </dl>

 

 
