---
title: Pour identifier les numéros de sortie
description: Pour identifier les numéros de sortie
ms.assetid: a2135a71-52e6-4f62-8be8-b9886be9b37c
keywords:
- Windows Media Format SDK, identifier les numéros de sortie
- ASF (Advanced Systems Format), identification des numéros de sortie
- ASF (format de systèmes avancés), identification des numéros de sortie
- ASF (Advanced Systems Format), nombres et formats de sortie
- ASF (format des systèmes avancés), nombres et formats de sortie
- nombres et formats de sortie, identification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c08f8e9a49d672efe7c04ecdde11ca4ef297d552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106509239"
---
# <a name="to-identify-output-numbers"></a><span data-ttu-id="734ca-109">Pour identifier les numéros de sortie</span><span class="sxs-lookup"><span data-stu-id="734ca-109">To Identify Output Numbers</span></span>

<span data-ttu-id="734ca-110">Pour identifier les numéros de sortie d’un fichier chargé, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="734ca-110">To identify the output numbers for a loaded file, perform the following steps.</span></span> <span data-ttu-id="734ca-111">Ces procédures sont identiques pour le lecteur asynchrone et le lecteur synchrone.</span><span class="sxs-lookup"><span data-stu-id="734ca-111">These procedures are identical for both the asynchronous reader and the synchronous reader.</span></span> <span data-ttu-id="734ca-112">Lorsque les noms d’interface varient, les méthodes de lecture synchrone sont répertoriées entre parenthèses après les méthodes du lecteur asynchrone.</span><span class="sxs-lookup"><span data-stu-id="734ca-112">Where interface names vary, the synchronous reader methods are listed in parentheses after the methods of the asynchronous reader.</span></span>

1.  <span data-ttu-id="734ca-113">Créez un objet lecteur et chargez un fichier pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="734ca-113">Create a reader object and load a file for reading.</span></span> <span data-ttu-id="734ca-114">Pour plus d’informations, consultez [pour créer un lecteur et ouvrir un fichier](to-create-a-reader-and-open-a-file.md) (ou [pour créer un lecteur synchrone et ouvrir un fichier](to-create-a-synchronous-reader-and-open-a-file.md)).</span><span class="sxs-lookup"><span data-stu-id="734ca-114">For more information, see [To Create a Reader and Open a File](to-create-a-reader-and-open-a-file.md) (or [To Create a Synchronous Reader and Open a File](to-create-a-synchronous-reader-and-open-a-file.md)).</span></span>
2.  <span data-ttu-id="734ca-115">Récupérez le nombre total de sorties pour le fichier en appelant [**IWMReader :: GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (ou [**IWMSyncReader :: GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)).</span><span class="sxs-lookup"><span data-stu-id="734ca-115">Retrieve the total number of outputs for the file by calling [**IWMReader::GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (or [**IWMSyncReader::GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)).</span></span>
3.  <span data-ttu-id="734ca-116">Parcourez les sorties une par une, en effectuant les étapes suivantes pour chacune d’elles :</span><span class="sxs-lookup"><span data-stu-id="734ca-116">Loop through the outputs one at a time, performing the following steps for each:</span></span>
    -   <span data-ttu-id="734ca-117">Récupérez l’interface [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) pour la sortie actuelle avec un appel à [**IWMReader :: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) (ou [**IWMSyncReader :: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)).</span><span class="sxs-lookup"><span data-stu-id="734ca-117">Retrieve the [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface for the current output with a call to [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) (or [**IWMSyncReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)).</span></span>
    -   <span data-ttu-id="734ca-118">Récupérez la structure du [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) pour la sortie en effectuant deux appels à [**IWMMediaProps :: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="734ca-118">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the output by making two calls to [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span></span> <span data-ttu-id="734ca-119">Effectuez le premier appel pour obtenir la taille de la structure, puis allouez de la mémoire pour celle-ci et transmettez un pointeur vers la mémoire allouée sur le deuxième appel.</span><span class="sxs-lookup"><span data-stu-id="734ca-119">Make the first call to get the size of the structure, then allocate memory for it and pass a pointer to the allocated memory on the second call.</span></span> <span data-ttu-id="734ca-120">Vous pouvez également appeler [**IWMMediaProps :: GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype), qui fournit le type principal sans que vous ayez besoin d’allouer de la mémoire pour la structure du **\_ \_ type de média WM** .</span><span class="sxs-lookup"><span data-stu-id="734ca-120">Alternatively, you can call [**IWMMediaProps::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype), which delivers the major type without requiring you to allocate memory for the **WM\_MEDIA\_TYPE** structure.</span></span> <span data-ttu-id="734ca-121">Vous pouvez ignorer les sorties d’un type majeur erroné.</span><span class="sxs-lookup"><span data-stu-id="734ca-121">You can skip outputs of the wrong major type.</span></span>
    -   <span data-ttu-id="734ca-122">Récupérez le type de média et le sous-type de média principaux à partir de la structure du **\_ \_ type de média WM** .</span><span class="sxs-lookup"><span data-stu-id="734ca-122">Retrieve the major media type and media subtype from the **WM\_MEDIA\_TYPE** structure.</span></span> <span data-ttu-id="734ca-123">Ces valeurs sont stockées dans les membres de données **MajorType** et **SubType** respectivement.</span><span class="sxs-lookup"><span data-stu-id="734ca-123">These values are stored in data members **majortype** and **subtype** respectively.</span></span>
    -   <span data-ttu-id="734ca-124">Vérifiez la valeur de **WM \_ Media \_ type. formatType**.</span><span class="sxs-lookup"><span data-stu-id="734ca-124">Check the value of **WM\_MEDIA\_TYPE.formattype**.</span></span> <span data-ttu-id="734ca-125">Spécifie le type de structure contenu dans la mémoire tampon au niveau du **\_ type de média WM \_ . pbFormat**.</span><span class="sxs-lookup"><span data-stu-id="734ca-125">This specifies the type of structure contained in the buffer at **WM\_MEDIA\_TYPE.pbFormat**.</span></span> <span data-ttu-id="734ca-126">Pour plus d’informations sur les types de format, consultez [types de médias](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="734ca-126">For more information about format types, see [Media Types](media-types.md).</span></span>
    -   <span data-ttu-id="734ca-127">Allouez de la mémoire pour contenir la structure du type identifié à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="734ca-127">Allocate memory to hold the structure of the type identified in the previous step.</span></span> <span data-ttu-id="734ca-128">Copiez la structure dans votre mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="734ca-128">Copy the structure to your allocated memory.</span></span> <span data-ttu-id="734ca-129">Pour l’audio et la vidéo, cette structure vous donne des informations essentielles sur la façon dont les données doivent être rendues.</span><span class="sxs-lookup"><span data-stu-id="734ca-129">For audio and video, this structure gives you essential information about how the data should be rendered.</span></span>

<span data-ttu-id="734ca-130">Le lecteur synchrone fournit également des méthodes pour récupérer des associations entre les numéros de sortie et les numéros de flux.</span><span class="sxs-lookup"><span data-stu-id="734ca-130">The synchronous reader also provides methods to retrieve associations between output numbers and stream numbers.</span></span> <span data-ttu-id="734ca-131">Pour plus d’informations, consultez [pour rechercher des numéros de flux et des numéros de sortie](to-find-stream-numbers-and-output-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="734ca-131">For more information, see [To Find Stream Numbers and Output Numbers](to-find-stream-numbers-and-output-numbers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="734ca-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="734ca-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="734ca-133">**Entrées, flux et sorties**</span><span class="sxs-lookup"><span data-stu-id="734ca-133">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="734ca-134">**Interface IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="734ca-134">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="734ca-135">**Interface IWMOutputMediaProps**</span><span class="sxs-lookup"><span data-stu-id="734ca-135">**IWMOutputMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[<span data-ttu-id="734ca-136">**Interface IWMReader**</span><span class="sxs-lookup"><span data-stu-id="734ca-136">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="734ca-137">**Interface IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="734ca-137">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="734ca-138">**Utilisation des sorties**</span><span class="sxs-lookup"><span data-stu-id="734ca-138">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




