---
title: Conversion de données d’un format à un autre
description: Conversion de données d’un format à un autre
ms.assetid: df995b7d-ac45-4964-a1b0-efd079c0c010
keywords:
- Gestionnaire de compression audio (ACM), conversion de données
- ACM (gestionnaire de compression audio), conversion de données
- Exemples ACM, conversion de données
- convertir des données
- acmStreamOpen fonction)
- acmStreamSize fonction)
- acmStreamPrepareHeader fonction)
- acmStreamConvert fonction)
- acmStreamUnprepareHeader fonction)
- acmStreamClose fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9645342aa9f19b2c31de77dc9d1031122ed0b2ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309918"
---
# <a name="converting-data-from-one-format-to-another"></a><span data-ttu-id="43f00-113">Conversion de données d’un format à un autre</span><span class="sxs-lookup"><span data-stu-id="43f00-113">Converting Data from One Format to Another</span></span>

<span data-ttu-id="43f00-114">L’ACM utilise des fonctions de flux pour prendre en charge la conversion de format de données.</span><span class="sxs-lookup"><span data-stu-id="43f00-114">The ACM uses stream functions to support data format conversion.</span></span> <span data-ttu-id="43f00-115">Les convertisseurs dans l’ACM modifient le format, mais pas le type de données.</span><span class="sxs-lookup"><span data-stu-id="43f00-115">Converters in the ACM change the format, but not the data type.</span></span> <span data-ttu-id="43f00-116">Par exemple, un module de conversion peut remplacer les données 44-kHz, 16 bits par des données 8 bits 44-kHz.</span><span class="sxs-lookup"><span data-stu-id="43f00-116">For example, a converter module can change 44-kHz, 16-bit data to 44-kHz, 8-bit data.</span></span>

<span data-ttu-id="43f00-117">Les fonctions ACM suivantes prennent en charge la conversion de format de données.</span><span class="sxs-lookup"><span data-stu-id="43f00-117">The following ACM functions support data format conversion.</span></span> <span data-ttu-id="43f00-118">Ils sont répertoriés dans l’ordre dans lequel vous les utilisez généralement.</span><span class="sxs-lookup"><span data-stu-id="43f00-118">They are listed in the order in which you would typically use them.</span></span>

-   <span data-ttu-id="43f00-119">La fonction [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) ouvre un flux de conversion.</span><span class="sxs-lookup"><span data-stu-id="43f00-119">The [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) function opens a conversion stream.</span></span>
-   <span data-ttu-id="43f00-120">La fonction [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) calcule la taille appropriée de la mémoire tampon source ou de destination.</span><span class="sxs-lookup"><span data-stu-id="43f00-120">The [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) function calculates the appropriate size of the source or destination buffer.</span></span>
-   <span data-ttu-id="43f00-121">La fonction [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader) prépare les mémoires tampons sources et de destination à utiliser dans une conversion.</span><span class="sxs-lookup"><span data-stu-id="43f00-121">The [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader) function prepares source and destination buffers to be used in a conversion.</span></span>
-   <span data-ttu-id="43f00-122">La fonction [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) convertit les données d’une mémoire tampon source au format de destination, en écrivant les données converties dans la mémoire tampon de destination.</span><span class="sxs-lookup"><span data-stu-id="43f00-122">The [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) function converts data in a source buffer into the destination format, writing the converted data into the destination buffer.</span></span>
-   <span data-ttu-id="43f00-123">La fonction [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) nettoie les mémoires tampons sources et de destination préparées par **acmStreamPrepareHeader**.</span><span class="sxs-lookup"><span data-stu-id="43f00-123">The [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) function cleans up the source and destination buffers prepared by **acmStreamPrepareHeader**.</span></span> <span data-ttu-id="43f00-124">Vous devez appeler cette fonction avant de libérer les mémoires tampons sources et de destination.</span><span class="sxs-lookup"><span data-stu-id="43f00-124">You must call this function before freeing the source and destination buffers.</span></span>
-   <span data-ttu-id="43f00-125">La fonction [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) ferme un flux de conversion.</span><span class="sxs-lookup"><span data-stu-id="43f00-125">The [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) function closes a conversion stream.</span></span>

<span data-ttu-id="43f00-126">Lors de la conversion de données, identifiez d’abord le format source, puis choisissez le format de destination.</span><span class="sxs-lookup"><span data-stu-id="43f00-126">When converting data, first identify the source format, then choose the destination format.</span></span> <span data-ttu-id="43f00-127">Pour ce faire, la méthode la plus simple consiste à utiliser la fonction [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , qui affiche une boîte de dialogue de sélection de format et retourne le choix de format de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="43f00-127">The easiest way to do this is by using the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, which displays a format-selection dialog box and returns the user's format choice.</span></span>

<span data-ttu-id="43f00-128">Lorsque vous connaissez les formats source et de destination, vous pouvez utiliser [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) pour ouvrir un flux de conversion.</span><span class="sxs-lookup"><span data-stu-id="43f00-128">When you know the source and destination formats, you can use [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) to open a conversion stream.</span></span> <span data-ttu-id="43f00-129">Vous pouvez ensuite utiliser la fonction [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) pour déterminer les tailles de mémoire tampon appropriées.</span><span class="sxs-lookup"><span data-stu-id="43f00-129">Then you can use the [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) function to determine the appropriate buffer sizes.</span></span>

<span data-ttu-id="43f00-130">L’étape suivante consiste à préparer les mémoires tampons à utiliser dans la conversion à l’aide de [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader).</span><span class="sxs-lookup"><span data-stu-id="43f00-130">The next step is to prepare the buffers to be used in the conversion by using [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader).</span></span>

<span data-ttu-id="43f00-131">Pour effectuer la conversion, utilisez [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) jusqu’à ce que toutes les mémoires tampons aient été traitées.</span><span class="sxs-lookup"><span data-stu-id="43f00-131">To perform the conversion, use [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) until all the buffers have been processed.</span></span> <span data-ttu-id="43f00-132">Une fois la conversion terminée, utilisez [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) pour nettoyer les tampons, puis utilisez [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) pour fermer le flux de conversion.</span><span class="sxs-lookup"><span data-stu-id="43f00-132">When the conversion is complete, use [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) to clean up the buffers and then use [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) to close the conversion stream.</span></span>

 

 




