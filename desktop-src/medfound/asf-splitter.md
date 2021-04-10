---
description: Séparateur ASF
ms.assetid: 383b1cc6-4a77-4e0e-a766-6213c64b025c
title: Séparateur ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f61bcd17a81197106d2f7c43fa1fdc25d9da2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111887"
---
# <a name="asf-splitter"></a><span data-ttu-id="09ee7-103">Séparateur ASF</span><span class="sxs-lookup"><span data-stu-id="09ee7-103">ASF Splitter</span></span>

<span data-ttu-id="09ee7-104">L’objet *séparateur* ASF est un composant de couche WMContainer qui analyse l’objet de données ASF d’un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="09ee7-104">The ASF *splitter* object is a WMContainer layer component that parses the ASF Data Object of an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="09ee7-105">Vous pouvez utiliser le séparateur pour lire les paquets de données dans l’objet de données et générer des exemples de flux.</span><span class="sxs-lookup"><span data-stu-id="09ee7-105">You can use the splitter to read the data packets in the Data Object and generate stream samples.</span></span> <span data-ttu-id="09ee7-106">Pour plus d’informations sur la structure d’un fichier ASF, consultez [structure des fichiers ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="09ee7-106">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="09ee7-107">Le séparateur expose l’interface [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .</span><span class="sxs-lookup"><span data-stu-id="09ee7-107">The splitter exposes the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface.</span></span> <span data-ttu-id="09ee7-108">Le séparateur analyse les paquets de données ASF pour les flux sélectionnés et les reconditionne dans des exemples d’objets individuels qui exposent l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .</span><span class="sxs-lookup"><span data-stu-id="09ee7-108">The splitter parses ASF data packets for the selected streams and repackages them into individual sample objects that expose the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span> <span data-ttu-id="09ee7-109">Le séparateur est l’un des composants de niveau plateforme de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="09ee7-109">The splitter is one of the platform-level components of Media Foundation.</span></span> <span data-ttu-id="09ee7-110">La source de média ASF utilise le séparateur en interne pour analyser les fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="09ee7-110">The ASF media source uses the splitter internally to parse ASF files.</span></span>

<span data-ttu-id="09ee7-111">Le diagramme suivant illustre la génération d’exemples pour un fichier ASF par le biais du séparateur.</span><span class="sxs-lookup"><span data-stu-id="09ee7-111">The following diagram illustrates sample generation for an ASF file through the splitter.</span></span>

![Diagramme montrant l’exemple de génération d’un fichier ASF](images/1eb9789c-c586-4f44-b907-b086cf288cc1.gif)

<span data-ttu-id="09ee7-113">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="09ee7-113">This section contains the following topics:</span></span>



| <span data-ttu-id="09ee7-114">Rubrique</span><span class="sxs-lookup"><span data-stu-id="09ee7-114">Topic</span></span>                                                                                                                        | <span data-ttu-id="09ee7-115">Description</span><span class="sxs-lookup"><span data-stu-id="09ee7-115">Description</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="09ee7-116">Création de l’objet Splitter ASF</span><span class="sxs-lookup"><span data-stu-id="09ee7-116">Creating the ASF Splitter Object</span></span>](creating-the-asf-splitter-object.md)                                                     | <span data-ttu-id="09ee7-117">Comment créer et initialiser le séparateur.</span><span class="sxs-lookup"><span data-stu-id="09ee7-117">How to create and initialize the splitter.</span></span>                              |
| [<span data-ttu-id="09ee7-118">Configuration de l’objet Splitter ASF</span><span class="sxs-lookup"><span data-stu-id="09ee7-118">Configuring the ASF Splitter Object</span></span>](configuring-the-asf-splitter-object.md)                                               | <span data-ttu-id="09ee7-119">Paramètres de configuration pour le séparateur.</span><span class="sxs-lookup"><span data-stu-id="09ee7-119">Configuration settings for the splitter.</span></span>                                |
| [<span data-ttu-id="09ee7-120">Génération d’exemples de flux à partir d’un objet de données ASF existant</span><span class="sxs-lookup"><span data-stu-id="09ee7-120">Generating Stream Samples from an Existing ASF Data Object</span></span>](generating-stream-samples-from-an-existing-asf-data-object.md) | <span data-ttu-id="09ee7-121">Comment analyser l’objet de données ASF et générer des échantillons de vapeur Packet.</span><span class="sxs-lookup"><span data-stu-id="09ee7-121">How to parse the ASF Data Object and generate packetized steam samples.</span></span> |



 

<span data-ttu-id="09ee7-122">Le tableau suivant présente les attributs d’objet de données pertinents.</span><span class="sxs-lookup"><span data-stu-id="09ee7-122">The following table shows the relevant Data Object attributes.</span></span>



| <span data-ttu-id="09ee7-123">Attribut</span><span class="sxs-lookup"><span data-stu-id="09ee7-123">Attribute</span></span>                                                                                                    | <span data-ttu-id="09ee7-124">Description</span><span class="sxs-lookup"><span data-stu-id="09ee7-124">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09ee7-125">**\_paquets MF PD \_ ASF FM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="09ee7-125">**MF\_PD\_ASF\_FILEPROPERTIES\_PACKETS**</span></span>](mf-pd-asf-fileproperties-packets-attribute.md)                   | <span data-ttu-id="09ee7-126">Nombre de paquets de données dans l’objet de données ASF.</span><span class="sxs-lookup"><span data-stu-id="09ee7-126">Number of data packets in the ASF Data Object.</span></span>                                                       |
| [<span data-ttu-id="09ee7-127">**\_taille de \_ paquet min PD ASF \_ FichierPropriétés \_ Min \_ \_ .**</span><span class="sxs-lookup"><span data-stu-id="09ee7-127">**MF\_PD\_ASF\_FILEPROPERTIES\_MIN\_PACKET\_SIZE**</span></span>](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | <span data-ttu-id="09ee7-128">Taille minimale des paquets de données dans le fichier, en octets.</span><span class="sxs-lookup"><span data-stu-id="09ee7-128">Minimum size of the data packets in the file, in bytes.</span></span>                                              |
| [<span data-ttu-id="09ee7-129">**\_ \_ \_ \_ taille maximale des \_ paquets \_ MF PD ASF FichierPropriétés**</span><span class="sxs-lookup"><span data-stu-id="09ee7-129">**MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_PACKET\_SIZE**</span></span>](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | <span data-ttu-id="09ee7-130">Taille maximale des paquets de données dans le fichier, en octets</span><span class="sxs-lookup"><span data-stu-id="09ee7-130">Maximum size of the data packets in the file, in bytes</span></span>                                               |
| [<span data-ttu-id="09ee7-131">**\_longueur des \_ \_ données ASF \_ pour MF**</span><span class="sxs-lookup"><span data-stu-id="09ee7-131">**MF\_PD\_ASF\_DATA\_LENGTH**</span></span>](mf-pd-asf-data-length-attribute.md)                                         | <span data-ttu-id="09ee7-132">Taille de l’objet de données ASF, en octets.</span><span class="sxs-lookup"><span data-stu-id="09ee7-132">Size of the ASF Data Object, in bytes.</span></span>                                                               |
| [<span data-ttu-id="09ee7-133">**\_décalage de \_ \_ début de données ASF \_ \_ pour MF PD**</span><span class="sxs-lookup"><span data-stu-id="09ee7-133">**MF\_PD\_ASF\_DATA\_START\_OFFSET**</span></span>](mf-pd-asf-data-start-offset-attribute.md)                            | <span data-ttu-id="09ee7-134">Décalage, en octets, du premier paquet de données de l’objet de données ASF par rapport au début du fichier.</span><span class="sxs-lookup"><span data-stu-id="09ee7-134">Offset, in bytes, to the first data packet in the ASF Data Object relative to the start of the file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="09ee7-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="09ee7-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09ee7-136">Composants WMContainer ASF</span><span class="sxs-lookup"><span data-stu-id="09ee7-136">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="09ee7-137">Didacticiel : lecture d’un fichier ASF</span><span class="sxs-lookup"><span data-stu-id="09ee7-137">Tutorial: Reading an ASF File</span></span>](tutorial--reading-an-asf-file.md)
</dt> <dt>

[<span data-ttu-id="09ee7-138">Prise en charge ASF dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="09ee7-138">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



