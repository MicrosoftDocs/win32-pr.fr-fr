---
title: Pour créer un lecteur et ouvrir un fichier
description: Pour créer un lecteur et ouvrir un fichier
ms.assetid: 82b194d6-7cb7-4b88-9ed7-944b8b43bc29
keywords:
- ASF (Advanced Systems Format), création de lecteurs
- ASF (format avancé des systèmes), création de lecteurs
- ASF (Advanced Systems Format), ouvrir des fichiers
- ASF (format des systèmes avancés), ouvrir des fichiers
- lecteurs asynchrones, création
- lecteurs asynchrones, ouverture de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e714f51b56a7d9f3b18a774cd3b8c74bf05352
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724090"
---
# <a name="to-create-a-reader-and-open-a-file"></a><span data-ttu-id="e88e8-109">Pour créer un lecteur et ouvrir un fichier</span><span class="sxs-lookup"><span data-stu-id="e88e8-109">To Create a Reader and Open a File</span></span>

<span data-ttu-id="e88e8-110">Avant de pouvoir travailler avec le lecteur, vous devez créer un objet lecteur et charger un fichier en lecture.</span><span class="sxs-lookup"><span data-stu-id="e88e8-110">Before you can do any work with the reader, you will need to create a reader object and load a file for reading.</span></span> <span data-ttu-id="e88e8-111">Pour initialiser le lecteur et ouvrir un fichier, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="e88e8-111">To initialize the reader and open a file, perform the following steps.</span></span>

1.  <span data-ttu-id="e88e8-112">Créez un objet lecteur en appelant la fonction [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) .</span><span class="sxs-lookup"><span data-stu-id="e88e8-112">Create a reader object by calling the [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) function.</span></span> <span data-ttu-id="e88e8-113">Vous devez spécifier le niveau de gestion des droits souhaité pour le nouvel objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="e88e8-113">You must specify the desired level of rights management for the new reader object.</span></span> <span data-ttu-id="e88e8-114">Les modes disponibles sont répertoriés dans le type d’énumération des [**\_ droits WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) .</span><span class="sxs-lookup"><span data-stu-id="e88e8-114">The available modes are listed in the [**WMT\_RIGHTS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) enumeration type.</span></span>
2.  <span data-ttu-id="e88e8-115">Spécifiez un fichier à lire en appelant [**IWMReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open).</span><span class="sxs-lookup"><span data-stu-id="e88e8-115">Specify a file to read by calling [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open).</span></span> <span data-ttu-id="e88e8-116">Vous devez spécifier une interface de rappel de lecteur pour le lecteur à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e88e8-116">You must specify a reader callback interface for the reader to use.</span></span> <span data-ttu-id="e88e8-117">Pour plus d’informations sur le rappel de lecteur, consultez [pour implémenter des messages de lecture dans le rappel OnStatus](to-implement-reader-messages-in-the-onstatus-callback.md).</span><span class="sxs-lookup"><span data-stu-id="e88e8-117">For more information about the reader callback, see [To Implement Reader Messages in the OnStatus Callback](to-implement-reader-messages-in-the-onstatus-callback.md).</span></span>
3.  <span data-ttu-id="e88e8-118">Attendez que le lecteur ouvre le fichier.</span><span class="sxs-lookup"><span data-stu-id="e88e8-118">Wait for the reader to open the file.</span></span> <span data-ttu-id="e88e8-119">Quand vous appelez **Open** pour charger un fichier, il retourne presque immédiatement et continue le traitement sur un autre thread.</span><span class="sxs-lookup"><span data-stu-id="e88e8-119">When you call **Open** to load a file, it returns almost immediately and continues processing on another thread.</span></span> <span data-ttu-id="e88e8-120">Vous devez attendre que les opérations se terminent, en signalant un événement lorsque le rappel **OnStatus** reçoit le \_ message d’état ouvert WMT.</span><span class="sxs-lookup"><span data-stu-id="e88e8-120">You should wait for operations to complete, by signaling an event when the **OnStatus** callback receives the WMT\_OPENED status message.</span></span>

<span data-ttu-id="e88e8-121">Le lecteur prend également en charge l’utilisation de l’interface com **IStream** pour ouvrir des fichiers.</span><span class="sxs-lookup"><span data-stu-id="e88e8-121">The reader also supports the use of the **IStream** COM interface for opening files.</span></span> <span data-ttu-id="e88e8-122">Vous pouvez implémenter l’interface **IStream** comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="e88e8-122">You can implement the **IStream** interface any way you choose.</span></span> <span data-ttu-id="e88e8-123">Une fois le fichier souhaité ouvert dans **IStream**, vous pouvez suivre les étapes décrites ci-dessus, sauf que vous devez appeler [**IWMReaderAdvanced2 :: OpenStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream) au lieu de **IWMReader :: Open** à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="e88e8-123">After the desired file is opened in **IStream**, you can follow the steps listed above, except that you must call [**IWMReaderAdvanced2::OpenStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream) instead of **IWMReader::Open** in step 2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e88e8-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e88e8-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e88e8-125">**Interface IWMReader**</span><span class="sxs-lookup"><span data-stu-id="e88e8-125">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="e88e8-126">**Interface IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="e88e8-126">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[<span data-ttu-id="e88e8-127">**Interface IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="e88e8-127">**IWMStatusCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)
</dt> <dt>

[<span data-ttu-id="e88e8-128">**Lecture des fichiers avec le lecteur asynchrone**</span><span class="sxs-lookup"><span data-stu-id="e88e8-128">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="e88e8-129">**Utilisation des méthodes de rappel**</span><span class="sxs-lookup"><span data-stu-id="e88e8-129">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




