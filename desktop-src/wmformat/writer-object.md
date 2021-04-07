---
title: Auteur, objet
description: Auteur, objet
ms.assetid: 8058b7fe-7d02-4572-ad43-6867d4ceb7e9
keywords:
- Windows Media Format SDK, objets Writer
- ASF (Advanced Systems Format), objets Writer
- ASF (format des systèmes avancés), objets Writer
- objets, objets Writer
- objets Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42d4783a8330ac1f0f16bc2ca2de4e843cbacc06
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724122"
---
# <a name="writer-object"></a><span data-ttu-id="419ec-108">Auteur, objet</span><span class="sxs-lookup"><span data-stu-id="419ec-108">Writer Object</span></span>

<span data-ttu-id="419ec-109">L’objet Writer est utilisé pour écrire des fichiers multimédias numériques à l’aide de la structure de fichiers ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="419ec-109">The writer object is used to write digital media files using the advanced systems format (ASF) file structure.</span></span> <span data-ttu-id="419ec-110">Le processus d’écriture d’un fichier multimédia numérique implique de nombreuses étapes internes à l’enregistreur, qui coordonne la compression, la paquets de paquets et le multiplexage.</span><span class="sxs-lookup"><span data-stu-id="419ec-110">The process of writing a digital media file involves many steps internal to the writer, which coordinates compression, packetization, and multiplexing.</span></span>

<span data-ttu-id="419ec-111">L’objet Writer comprend des interfaces pour la sortie vers des fichiers ou un réseau, prend en charge une interface de rappel et peut créer un ou plusieurs objets de propriétés de média d’entrée.</span><span class="sxs-lookup"><span data-stu-id="419ec-111">The writer object includes interfaces for output to files or a network, supports one callback interface, and can create one or more input media properties objects.</span></span>

<span data-ttu-id="419ec-112">L’objet Writer est créé par la fonction [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter), qui définit un pointeur vers une interface **IWMWriter** .</span><span class="sxs-lookup"><span data-stu-id="419ec-112">The writer object is created by the function [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter), which sets a pointer to an **IWMWriter** interface.</span></span> <span data-ttu-id="419ec-113">Les autres interfaces de l’objet Writer peuvent être obtenues en appelant la méthode **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="419ec-113">The other interfaces of the writer object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="419ec-114">Les interfaces suivantes sont prises en charge par l’objet Writer.</span><span class="sxs-lookup"><span data-stu-id="419ec-114">The following interfaces are supported by the writer object.</span></span>



| <span data-ttu-id="419ec-115">Interface</span><span class="sxs-lookup"><span data-stu-id="419ec-115">Interface</span></span>                                          | <span data-ttu-id="419ec-116">Description</span><span class="sxs-lookup"><span data-stu-id="419ec-116">Description</span></span>                                                                                                                                                                                               |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="419ec-117">**IWMDRMWriter**</span><span class="sxs-lookup"><span data-stu-id="419ec-117">**IWMDRMWriter**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)               | <span data-ttu-id="419ec-118">Fournit des méthodes pour générer des clés [*DRM*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="419ec-118">Provides methods to generate [*DRM*](wmformat-glossary.md) keys.</span></span>                                                                                                |
| [<span data-ttu-id="419ec-119">**IWMDRMWriter2**</span><span class="sxs-lookup"><span data-stu-id="419ec-119">**IWMDRMWriter2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter2)             | <span data-ttu-id="419ec-120">Configure l’objet enregistreur pour écrire un fichier contenant un flux pré-chiffré conforme au protocole Windows Media DRM 10 pour les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="419ec-120">Configures the writer object to write a file containing a pre-encrypted stream that conforms to the Windows Media DRM 10 for Network Devices protocol.</span></span>                                                    |
| [<span data-ttu-id="419ec-121">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="419ec-121">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)             | <span data-ttu-id="419ec-122">Gère la spécification et la récupération des informations d’en-tête, telles que les métadonnées, les [*marqueurs*](wmformat-glossary.md), etc.</span><span class="sxs-lookup"><span data-stu-id="419ec-122">Manages the specification and retrieval of header information, such as metadata, [*markers*](wmformat-glossary.md), and so on.</span></span>                                                           |
| [<span data-ttu-id="419ec-123">**IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="419ec-123">**IWMHeaderInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)           | <span data-ttu-id="419ec-124">Gère l’énumération à l’aide des informations de codec disponibles.</span><span class="sxs-lookup"><span data-stu-id="419ec-124">Manages enumerating through the available codec information.</span></span> <span data-ttu-id="419ec-125">Hérite de toutes les méthodes de **IWMHeaderInfo**.</span><span class="sxs-lookup"><span data-stu-id="419ec-125">Inherits all of the methods of **IWMHeaderInfo**.</span></span>                                                                                            |
| [<span data-ttu-id="419ec-126">**IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="419ec-126">**IWMHeaderInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)           | <span data-ttu-id="419ec-127">Gère l’énumération à l’aide des informations de codec disponibles.</span><span class="sxs-lookup"><span data-stu-id="419ec-127">Manages enumerating through the available codec information.</span></span> <span data-ttu-id="419ec-128">Hérite de toutes les méthodes de **IWMHeaderInfo** et **IWMHeaderInfo2**.</span><span class="sxs-lookup"><span data-stu-id="419ec-128">Inherits all of the methods of **IWMHeaderInfo** and **IWMHeaderInfo2**.</span></span>                                                                     |
| [<span data-ttu-id="419ec-129">**IWMWatermarkInfo**</span><span class="sxs-lookup"><span data-stu-id="419ec-129">**IWMWatermarkInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo)       | <span data-ttu-id="419ec-130">Fournit un accès aux informations sur les systèmes de tatouage sur le système.</span><span class="sxs-lookup"><span data-stu-id="419ec-130">Provides access to information about watermarking systems present on the system.</span></span>                                                                                                                          |
| [<span data-ttu-id="419ec-131">**IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="419ec-131">**IWMWriter**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)                     | <span data-ttu-id="419ec-132">Démarre et arrête l’écriture des fichiers ASF ; Il comprend des méthodes pour allouer des mémoires tampons, définir et récupérer des propriétés d’entrée, définir des profils et des noms de fichiers de sortie et déverrouiller le writer.</span><span class="sxs-lookup"><span data-stu-id="419ec-132">Starts and stops the writing of ASF files; it includes methods for allocating buffers, setting and retrieving input properties, setting profiles and output file names, and unlocking the writer.</span></span>         |
| [<span data-ttu-id="419ec-133">**IWMWriterAdvanced**</span><span class="sxs-lookup"><span data-stu-id="419ec-133">**IWMWriterAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)     | <span data-ttu-id="419ec-134">Ajoute, obtient et supprime les objets récepteurs spécifiés ; Récupère les statistiques, le nombre de récepteurs et l’heure à laquelle l’enregistreur travaille ; et exécute d’autres fonctions avancées.</span><span class="sxs-lookup"><span data-stu-id="419ec-134">Adds, gets, and removes specified sink objects; retrieves statistics, number of sinks, and the clock time the writer is working to; and performs other advanced functions.</span></span>                                |
| [<span data-ttu-id="419ec-135">**IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="419ec-135">**IWMWriterAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)   | <span data-ttu-id="419ec-136">Fournit des fonctionnalités avancées, en particulier pour gérer la vidéo désentrelacée.</span><span class="sxs-lookup"><span data-stu-id="419ec-136">Provides some advanced functionality, particularly for handling deinterlaced video.</span></span> <span data-ttu-id="419ec-137">Hérite de toutes les méthodes de **IWMWriterAdvanced**.</span><span class="sxs-lookup"><span data-stu-id="419ec-137">Inherits all of the methods of **IWMWriterAdvanced**.</span></span>                                                                 |
| [<span data-ttu-id="419ec-138">**IWMWriterAdvanced3**</span><span class="sxs-lookup"><span data-stu-id="419ec-138">**IWMWriterAdvanced3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)   | <span data-ttu-id="419ec-139">Fournit des fonctionnalités d’écriture supplémentaires, notamment la possibilité d’obtenir des statistiques d’enregistreur détaillées.</span><span class="sxs-lookup"><span data-stu-id="419ec-139">Provides additional writer functionality, including the ability to get detailed writer statistics.</span></span> <span data-ttu-id="419ec-140">Hérite de toutes les méthodes de **IWMWriterAdvanced** et **IWMWriterAdvanced2**.</span><span class="sxs-lookup"><span data-stu-id="419ec-140">Inherits all of the methods of **IWMWriterAdvanced** and **IWMWriterAdvanced2**.</span></span>                       |
| [<span data-ttu-id="419ec-141">**IWMWriterPostView**</span><span class="sxs-lookup"><span data-stu-id="419ec-141">**IWMWriterPostView**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview)     | <span data-ttu-id="419ec-142">Gère certaines fonctionnalités d’écriture avancées relatives aux exemples postviewing.</span><span class="sxs-lookup"><span data-stu-id="419ec-142">Manages some advanced writing functionality related to postviewing samples.</span></span> <span data-ttu-id="419ec-143">Postviewing affiche la sortie, généralement à partir d’un encodeur, pour vérifier que le processus d’encodage/décodage fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="419ec-143">Postviewing is viewing the output, usually from an encoder, to check that the encoding/decoding process is working correctly.</span></span> |
| [<span data-ttu-id="419ec-144">**IWMWriterPreprocess**</span><span class="sxs-lookup"><span data-stu-id="419ec-144">**IWMWriterPreprocess**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) | <span data-ttu-id="419ec-145">Gère les passes de prétraitement effectuées par le writer.</span><span class="sxs-lookup"><span data-stu-id="419ec-145">Manages preprocessing passes made by the writer.</span></span> <span data-ttu-id="419ec-146">Les passes de prétraitement sont utilisées pour améliorer la qualité de la sortie encodée.</span><span class="sxs-lookup"><span data-stu-id="419ec-146">Preprocessing passes are used to improve the quality of encoded output.</span></span>                                                                                  |



 

<span data-ttu-id="419ec-147">L’interface de rappel suivante doit être implémentée par l’application pour suivre la progression de postviewing.</span><span class="sxs-lookup"><span data-stu-id="419ec-147">The following callback interface must be implemented by the application to track the progress of postviewing.</span></span>



| <span data-ttu-id="419ec-148">Interface</span><span class="sxs-lookup"><span data-stu-id="419ec-148">Interface</span></span>                                                      | <span data-ttu-id="419ec-149">Description</span><span class="sxs-lookup"><span data-stu-id="419ec-149">Description</span></span>                                                                                              |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="419ec-150">**IWMWriterPostViewCallback**</span><span class="sxs-lookup"><span data-stu-id="419ec-150">**IWMWriterPostViewCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback) | <span data-ttu-id="419ec-151">Gère le mode de réception des exemples non compressés de l’objet Writer pour afficher un aperçu de ce que fait le codec.</span><span class="sxs-lookup"><span data-stu-id="419ec-151">Manages how uncompressed samples are received from the writer object to preview what the codec is doing.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="419ec-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="419ec-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="419ec-153">**Objets**</span><span class="sxs-lookup"><span data-stu-id="419ec-153">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="419ec-154">**Écriture de fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="419ec-154">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




