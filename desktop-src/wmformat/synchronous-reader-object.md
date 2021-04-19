---
title: Lecteur synchrone, objet
description: Lecteur synchrone, objet
ms.assetid: 52a4891f-03bf-4d8a-ab7b-e9739db30bc3
keywords:
- Windows Media Format SDK, objets lecteur synchrones
- ASF (Advanced Systems Format), objets lecteur synchrones
- ASF (format des systèmes avancés), objets lecteur synchrones
- objets, lecteurs synchrones
- lecteurs synchrones, objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491fed915a049dbfc52acc24d06a0344d8e3109c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "106510671"
---
# <a name="synchronous-reader-object"></a><span data-ttu-id="d6c80-108">Lecteur synchrone, objet</span><span class="sxs-lookup"><span data-stu-id="d6c80-108">Synchronous Reader Object</span></span>

<span data-ttu-id="d6c80-109">L’objet lecteur synchrone est utilisé pour lire des fichiers multimédias numériques à l’aide d’appels synchrones.</span><span class="sxs-lookup"><span data-stu-id="d6c80-109">The synchronous reader object is used to read digital media files by using synchronous calls.</span></span>

<span data-ttu-id="d6c80-110">L’objet lecteur synchrone est créé par la fonction [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader), qui définit un pointeur vers une interface **IWMSyncReader** .</span><span class="sxs-lookup"><span data-stu-id="d6c80-110">The synchronous reader object is created by the function [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader), which sets a pointer to an **IWMSyncReader** interface.</span></span> <span data-ttu-id="d6c80-111">Les autres interfaces prises en charge par l’interface de lecture synchrone peuvent être obtenues en appelant la méthode **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="d6c80-111">The other interfaces supported by the synchronous reader interface can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="d6c80-112">Les interfaces suivantes sont prises en charge par l’objet lecteur synchrone.</span><span class="sxs-lookup"><span data-stu-id="d6c80-112">The following interfaces are supported by the synchronous reader object.</span></span>



| <span data-ttu-id="d6c80-113">Interface</span><span class="sxs-lookup"><span data-stu-id="d6c80-113">Interface</span></span>                                | <span data-ttu-id="d6c80-114">Description</span><span class="sxs-lookup"><span data-stu-id="d6c80-114">Description</span></span>                                                                                                                                                        |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6c80-115">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="d6c80-115">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)   | <span data-ttu-id="d6c80-116">Définit et récupère les informations d’en-tête, telles que les métadonnées, les [*marqueurs*](wmformat-glossary.md), etc.</span><span class="sxs-lookup"><span data-stu-id="d6c80-116">Sets and retrieves header information, such as metadata, [*markers*](wmformat-glossary.md), and so on.</span></span>                                            |
| [<span data-ttu-id="d6c80-117">**IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="d6c80-117">**IWMHeaderInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) | <span data-ttu-id="d6c80-118">Énumère les informations de codec disponibles.</span><span class="sxs-lookup"><span data-stu-id="d6c80-118">Enumerates the available codec information.</span></span> <span data-ttu-id="d6c80-119">Hérite de toutes les méthodes de **IWMHeaderInfo**.</span><span class="sxs-lookup"><span data-stu-id="d6c80-119">Inherits all of the methods of **IWMHeaderInfo**.</span></span>                                                                      |
| [<span data-ttu-id="d6c80-120">**IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="d6c80-120">**IWMHeaderInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) | <span data-ttu-id="d6c80-121">Prend en charge des tailles d’attribut volumineuses, des noms d’attributs dupliqués et la prise en charge de plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="d6c80-121">Supports large attribute sizes, duplicate attribute names, and multiple language support.</span></span> <span data-ttu-id="d6c80-122">Hérite de toutes les méthodes de **IWMHeaderInfo** et **IWMHeaderInfo2**.</span><span class="sxs-lookup"><span data-stu-id="d6c80-122">Inherits all of the methods of **IWMHeaderInfo** and **IWMHeaderInfo2**.</span></span> |
| [<span data-ttu-id="d6c80-123">**IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="d6c80-123">**IWMProfile**</span></span>](iwmprofile.md)         | <span data-ttu-id="d6c80-124">Fournit l’accès aux informations de profil du fichier Windows Media chargé dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="d6c80-124">Provides access to the profile information of the Windows Media file loaded into the reader.</span></span>                                                                       |
| [<span data-ttu-id="d6c80-125">**IWMProfile2**</span><span class="sxs-lookup"><span data-stu-id="d6c80-125">**IWMProfile2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)       | <span data-ttu-id="d6c80-126">Récupère l’identificateur global unique (GUID), le cas échéant, associé au profil.</span><span class="sxs-lookup"><span data-stu-id="d6c80-126">Retrieves the globally unique identifier (GUID), if any, associated with the profile.</span></span> <span data-ttu-id="d6c80-127">Hérite de toutes les méthodes de **IWMProfile**.</span><span class="sxs-lookup"><span data-stu-id="d6c80-127">Inherits all of the methods of **IWMProfile**.</span></span>                               |
| [<span data-ttu-id="d6c80-128">**IWMProfile3**</span><span class="sxs-lookup"><span data-stu-id="d6c80-128">**IWMProfile3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)       | <span data-ttu-id="d6c80-129">Prend en charge le partage de bande passante et les informations de hiérarchisation des flux dans le profil.</span><span class="sxs-lookup"><span data-stu-id="d6c80-129">Supports bandwidth sharing and stream prioritization information in the profile.</span></span> <span data-ttu-id="d6c80-130">Hérite de toutes les méthodes de **IWMProfile** et **IWMProfile2**.</span><span class="sxs-lookup"><span data-stu-id="d6c80-130">Inherits all of the methods of **IWMProfile** and **IWMProfile2**.</span></span>                |
| [<span data-ttu-id="d6c80-131">**IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="d6c80-131">**IWMSyncReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)   | <span data-ttu-id="d6c80-132">Fournit des fonctionnalités de lecture synchrones pour les fichiers multimédias numériques.</span><span class="sxs-lookup"><span data-stu-id="d6c80-132">Provides synchronous reading capabilities for digital media files.</span></span>                                                                                                 |
| [<span data-ttu-id="d6c80-133">**IWMSyncReader2**</span><span class="sxs-lookup"><span data-stu-id="d6c80-133">**IWMSyncReader2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader2) | <span data-ttu-id="d6c80-134">Prend en charge la recherche de codes temporels SMPTE et l’allocation manuelle des exemples.</span><span class="sxs-lookup"><span data-stu-id="d6c80-134">Provides support for seeking to SMPTE time codes and for allocating samples manually.</span></span> <span data-ttu-id="d6c80-135">Hérite de toutes les méthodes de **IWMSyncReader**.</span><span class="sxs-lookup"><span data-stu-id="d6c80-135">Inherits all of the methods of **IWMSyncReader**.</span></span>                            |



 

## <a name="related-topics"></a><span data-ttu-id="d6c80-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d6c80-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6c80-137">**Objets**</span><span class="sxs-lookup"><span data-stu-id="d6c80-137">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="d6c80-138">**Lecteur, objet**</span><span class="sxs-lookup"><span data-stu-id="d6c80-138">**Reader Object**</span></span>](reader-object.md)
</dt> <dt>

[<span data-ttu-id="d6c80-139">**Lecture des fichiers avec le lecteur synchrone**</span><span class="sxs-lookup"><span data-stu-id="d6c80-139">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




