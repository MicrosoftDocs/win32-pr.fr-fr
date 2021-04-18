---
title: Assigner des formats de sortie
description: Assigner des formats de sortie
ms.assetid: 47697ffb-51cb-44cd-a0b0-7d85625a38f9
keywords:
- Windows Media Format SDK, assigner des formats de sortie
- ASF (Advanced Systems Format), assigner des formats de sortie
- ASF (format des systèmes avancés), assigner des formats de sortie
- ASF (Advanced Systems Format), nombres et formats de sortie
- ASF (format des systèmes avancés), nombres et formats de sortie
- nombres et formats de sortie, affectation
- codecs, nombres et formats de sortie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633673053a2b34a2f7aed5ed3f6ae66457a7ee13
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "106511880"
---
# <a name="assigning-output-formats"></a><span data-ttu-id="50c71-110">Assigner des formats de sortie</span><span class="sxs-lookup"><span data-stu-id="50c71-110">Assigning Output Formats</span></span>

<span data-ttu-id="50c71-111">Certains codecs peuvent décompresser les données multimédias numériques dans plusieurs formats non compressés.</span><span class="sxs-lookup"><span data-stu-id="50c71-111">Some codecs can decompress digital media data into several uncompressed formats.</span></span> <span data-ttu-id="50c71-112">Vous pouvez rechercher tous les formats pris en charge pour une sortie spécifique à l’aide du lecteur asynchrone ou du lecteur synchrone.</span><span class="sxs-lookup"><span data-stu-id="50c71-112">You can find all of the supported formats for a specific output using either the asynchronous reader or the synchronous reader.</span></span>

<span data-ttu-id="50c71-113">Pour examiner tous les formats disponibles pour une sortie, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="50c71-113">To examine all of the available formats for an output, perform the following steps.</span></span> <span data-ttu-id="50c71-114">Ces procédures sont identiques pour le lecteur asynchrone et le lecteur synchrone.</span><span class="sxs-lookup"><span data-stu-id="50c71-114">These procedures are identical for both the asynchronous reader and the synchronous reader.</span></span> <span data-ttu-id="50c71-115">Lorsque les noms d’interface varient, les méthodes de lecture synchrone sont répertoriées entre parenthèses après les méthodes du lecteur asynchrone.</span><span class="sxs-lookup"><span data-stu-id="50c71-115">Where interface names vary, the synchronous reader methods are listed in parentheses after the methods of the asynchronous reader.</span></span>

1.  <span data-ttu-id="50c71-116">Créez un objet lecteur et chargez un fichier pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="50c71-116">Create a reader object and load a file for reading.</span></span> <span data-ttu-id="50c71-117">Pour plus d’informations, consultez [pour créer un lecteur et ouvrir un fichier](to-create-a-reader-and-open-a-file.md) (ou [pour créer un lecteur synchrone et ouvrir un fichier](to-create-a-synchronous-reader-and-open-a-file.md)).</span><span class="sxs-lookup"><span data-stu-id="50c71-117">For more information, see [To Create a Reader and Open a File](to-create-a-reader-and-open-a-file.md) (or [To Create a Synchronous Reader and Open a File](to-create-a-synchronous-reader-and-open-a-file.md)).</span></span>
2.  <span data-ttu-id="50c71-118">Déterminez la sortie pour laquelle vous souhaitez rechercher les formats disponibles.</span><span class="sxs-lookup"><span data-stu-id="50c71-118">Determine the output for which you want to find the available formats.</span></span> <span data-ttu-id="50c71-119">Si vous ne connaissez pas encore la sortie que vous souhaitez utiliser, vous pouvez identifier les sorties dans le fichier à l’aide des procédures décrites dans [pour identifier les numéros de sortie](to-identify-output-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="50c71-119">If you don't already know which output you want to use, you can identify the outputs in the file using the procedures in [To Identify Output Numbers](to-identify-output-numbers.md).</span></span>
3.  <span data-ttu-id="50c71-120">Récupérez le nombre total de formats disponibles pour la sortie souhaitée en appelant [**IWMReader :: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (ou [**IWMSyncReader :: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)).</span><span class="sxs-lookup"><span data-stu-id="50c71-120">Retrieve the total number of available formats for the desired output by calling [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (or [**IWMSyncReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)).</span></span>
4.  <span data-ttu-id="50c71-121">Parcourez les formats disponibles l’un après l’autre, en effectuant les étapes suivantes pour chacun d’entre eux :</span><span class="sxs-lookup"><span data-stu-id="50c71-121">Loop through the available formats one at a time, performing the following steps for each:</span></span>
    -   <span data-ttu-id="50c71-122">Récupérez l’interface [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) pour le format de sortie actuel en appelant [**IWMReader :: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (ou [**IWMSyncReader :: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)).</span><span class="sxs-lookup"><span data-stu-id="50c71-122">Retrieve the [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface for the current output format by calling [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (or [**IWMSyncReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)).</span></span>
    -   <span data-ttu-id="50c71-123">Récupérez la structure du [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) pour le format de sortie en effectuant deux appels à [**IWMMediaProps :: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="50c71-123">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the output format by making two calls to [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span></span> <span data-ttu-id="50c71-124">Effectuez le premier appel pour obtenir la taille de la structure, puis allouez de la mémoire pour celle-ci et transmettez un pointeur vers la mémoire allouée sur le deuxième appel.</span><span class="sxs-lookup"><span data-stu-id="50c71-124">Make the first call to get the size of the structure, then allocate memory for it and pass a pointer to the allocated memory on the second call.</span></span>
    -   <span data-ttu-id="50c71-125">Recherchez le sous-type de média du format de sortie dans **WM \_ Media \_ type. SubType**.</span><span class="sxs-lookup"><span data-stu-id="50c71-125">Find the media subtype of the output format in **WM\_MEDIA\_TYPE.subtype**.</span></span>
    -   <span data-ttu-id="50c71-126">Pour la vidéo, si le sous-type actuel est le format que vous souhaitez utiliser pour la sortie, quittez la boucle.</span><span class="sxs-lookup"><span data-stu-id="50c71-126">For video, if the current subtype is the format you want to use for output, break out of the loop.</span></span> <span data-ttu-id="50c71-127">Sinon, passez à l’itération suivante.</span><span class="sxs-lookup"><span data-stu-id="50c71-127">Otherwise go to the next iteration.</span></span>

        <span data-ttu-id="50c71-128">Pour l’audio, vous devez vérifier les valeurs de la structure **WAVEFORMATEX** en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="50c71-128">For audio, you must check the values in the **WAVEFORMATEX** structure against your requirements.</span></span> <span data-ttu-id="50c71-129">**WM \_ MEDIA \_ type. pbFormat** pointe vers la structure **WAVEFORMATEX** pour les sorties audio.</span><span class="sxs-lookup"><span data-stu-id="50c71-129">**WM\_MEDIA\_TYPE.pbFormat** points to the **WAVEFORMATEX** structure for audio outputs.</span></span>

5.  <span data-ttu-id="50c71-130">Une fois que vous avez trouvé la sortie souhaitée, définissez-la pour l’utiliser avec le lecteur en appelant [**IWMReader :: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (ou [**IWMSyncReader :: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)).</span><span class="sxs-lookup"><span data-stu-id="50c71-130">When you have found the output desired, set it for use with the reader by calling [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (or [**IWMSyncReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)).</span></span> <span data-ttu-id="50c71-131">Vous devez passer un pointeur vers l’interface **IWMOutputMediaProps** obtenue à la première étape de la boucle.</span><span class="sxs-lookup"><span data-stu-id="50c71-131">You must pass a pointer to the **IWMOutputMediaProps** interface obtained in the first step of the loop.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50c71-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50c71-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50c71-133">**Interface IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="50c71-133">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="50c71-134">**Interface IWMOutputMediaProps**</span><span class="sxs-lookup"><span data-stu-id="50c71-134">**IWMOutputMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[<span data-ttu-id="50c71-135">**Interface IWMReader**</span><span class="sxs-lookup"><span data-stu-id="50c71-135">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="50c71-136">**Interface IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="50c71-136">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="50c71-137">**Utilisation des sorties**</span><span class="sxs-lookup"><span data-stu-id="50c71-137">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




