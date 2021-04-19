---
title: Pour créer un lecteur synchrone et ouvrir un fichier
description: Pour créer un lecteur synchrone et ouvrir un fichier
ms.assetid: 6349d05e-20db-4ce8-83fd-cad4cec666f2
keywords:
- ASF (Advanced Systems Format), création de lecteurs
- ASF (format avancé des systèmes), création de lecteurs
- ASF (Advanced Systems Format), ouvrir des fichiers
- ASF (format des systèmes avancés), ouvrir des fichiers
- lecteurs synchrones, création
- lecteurs synchrones, ouverture de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e222c046a685885fa9e17baa52d0161176551ff3
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "106509839"
---
# <a name="to-create-a-synchronous-reader-and-open-a-file"></a><span data-ttu-id="83517-109">Pour créer un lecteur synchrone et ouvrir un fichier</span><span class="sxs-lookup"><span data-stu-id="83517-109">To Create a Synchronous Reader and Open a File</span></span>

<span data-ttu-id="83517-110">Avant de pouvoir travailler avec le lecteur synchrone, vous devez créer un objet lecteur synchrone et charger un fichier en lecture.</span><span class="sxs-lookup"><span data-stu-id="83517-110">Before you can do any work with the synchronous reader, you will need to create a synchronous reader object and load a file for reading.</span></span> <span data-ttu-id="83517-111">Pour initialiser le lecteur synchrone et ouvrir un fichier, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="83517-111">To initialize the synchronous reader and open a file, perform the following steps.</span></span>

1.  <span data-ttu-id="83517-112">Créez un objet lecteur synchrone en appelant la fonction [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) .</span><span class="sxs-lookup"><span data-stu-id="83517-112">Create a synchronous reader object by calling the [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) function.</span></span> <span data-ttu-id="83517-113">Vous devez spécifier le niveau de gestion des droits souhaité pour le nouvel objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="83517-113">You must specify the desired level of rights management for the new reader object.</span></span> <span data-ttu-id="83517-114">Les modes disponibles sont répertoriés dans le type d’énumération des **\_ droits WMT** .</span><span class="sxs-lookup"><span data-stu-id="83517-114">The available modes are listed in the **WMT\_RIGHTS** enumeration type.</span></span>
2.  <span data-ttu-id="83517-115">Spécifiez un fichier à lire en appelant [**IWMSyncReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).</span><span class="sxs-lookup"><span data-stu-id="83517-115">Specify a file to read by calling [**IWMSyncReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).</span></span>

<span data-ttu-id="83517-116">Le lecteur synchrone prend également en charge l’utilisation de l’interface com **IStream** pour ouvrir des fichiers.</span><span class="sxs-lookup"><span data-stu-id="83517-116">The synchronous reader also supports the use of the **IStream** COM interface for opening files.</span></span> <span data-ttu-id="83517-117">Vous pouvez implémenter l’interface **IStream** comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="83517-117">You can implement the **IStream** interface any way you choose.</span></span> <span data-ttu-id="83517-118">Une fois le fichier souhaité ouvert dans **IStream**, vous pouvez suivre les étapes décrites ci-dessus, sauf que vous devez appeler [**IWMSyncReader :: OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) au lieu de **IWMSyncReader :: Open** à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="83517-118">After the desired file is opened in **IStream**, you can follow the steps listed above, except that you must call [**IWMSyncReader::OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) instead of **IWMSyncReader::Open** in step 2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83517-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="83517-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83517-120">**Interface IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="83517-120">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="83517-121">**Lecture des fichiers avec le lecteur synchrone**</span><span class="sxs-lookup"><span data-stu-id="83517-121">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




