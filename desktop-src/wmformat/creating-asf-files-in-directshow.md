---
title: Création de fichiers ASF dans DirectShow (kit de développement logiciel (SDK) Windows Media format 11)
description: Création de fichiers ASF dans DirectShow
ms.assetid: 8b7af340-934d-43a9-88e9-7bbb2d3a38e0
keywords:
- Windows Media Format SDK, création de fichiers ASF dans DirectShow
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- ASF (Advanced Systems Format), création dans DirectShow
- ASF (format de systèmes avancés), création dans DirectShow
- DirectShow, création de fichiers ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbe4a6a37a508e5d7c713ae4cf38d771d075cefa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102664"
---
# <a name="creating-asf-files-in-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="15b84-110">Création de fichiers ASF dans DirectShow (kit de développement logiciel (SDK) Windows Media format 11)</span><span class="sxs-lookup"><span data-stu-id="15b84-110">Creating ASF Files in DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="15b84-111">Vous pouvez utiliser DirectShow pour créer des fichiers ASF directement à partir de sources de capture telles que des caméscopes DV ou pour transcoder d’autres fichiers au format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="15b84-111">You can use DirectShow to create ASF files directly from capture sources such as DV camcorders or to transcode other files into Windows Media Format.</span></span> <span data-ttu-id="15b84-112">Dans l’un ou l’autre scénario, les applications créent des graphiques de filtre qui incluent le filtre d' [enregistreur ASF WM](wm-asf-writer-filter.md) comme convertisseur.</span><span class="sxs-lookup"><span data-stu-id="15b84-112">In either scenario, applications create filter graphs that include the [WM ASF Writer](wm-asf-writer-filter.md) filter as the renderer.</span></span>

<span data-ttu-id="15b84-113">L’enregistreur ASF WM fournit un wrapper partiel pour le kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="15b84-113">The WM ASF Writer provides a partial wrapper for the Windows Media Format SDK.</span></span> <span data-ttu-id="15b84-114">Les applications peuvent utiliser l’interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) du filtre pour passer un profil système (versions 4, 7 ou 8), ou utiliser le kit de développement logiciel (SDK) du format Windows Media directement pour créer un profil personnalisé à passer au filtre.</span><span class="sxs-lookup"><span data-stu-id="15b84-114">Applications can use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface of the filter to pass in a system profile (versions 4, 7, or 8), or use the Windows Media Format SDK directly to create a custom profile to pass to the filter.</span></span> <span data-ttu-id="15b84-115">Pour ajouter des métadonnées et d’autres informations d’en-tête, l’application utilise l’interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) , qui peut être obtenue à partir du filtre.</span><span class="sxs-lookup"><span data-stu-id="15b84-115">To add metadata and other header information, the application uses the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface, which can be obtained from the filter.</span></span> <span data-ttu-id="15b84-116">Une fois le profil et les métadonnées configurés, l’application peut simplement exécuter le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="15b84-116">After the profile and metadata have been configured, the application can simply run the filter graph.</span></span> <span data-ttu-id="15b84-117">En interne, le filtre utilise le kit de développement logiciel (SDK) Windows Media format pour écrire le fichier.</span><span class="sxs-lookup"><span data-stu-id="15b84-117">Internally, the filter uses the Windows Media Format SDK to write the file.</span></span> <span data-ttu-id="15b84-118">Le filtre gère tous les détails de synchronisation audio-vidéo, qui seraient autrement la responsabilité de l’application.</span><span class="sxs-lookup"><span data-stu-id="15b84-118">The filter handles all the audio-video synchronization details, which would otherwise be the responsibility of the application.</span></span>

<span data-ttu-id="15b84-119">Ce processus est expliqué plus en détail dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="15b84-119">This process is explained in more detail in the following sections.</span></span>



| <span data-ttu-id="15b84-120">Section</span><span class="sxs-lookup"><span data-stu-id="15b84-120">Section</span></span>                                                                                                           | <span data-ttu-id="15b84-121">Description</span><span class="sxs-lookup"><span data-stu-id="15b84-121">Description</span></span>                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="15b84-122">Configuration de l’enregistreur ASF de WM (QASF)</span><span class="sxs-lookup"><span data-stu-id="15b84-122">Configuring the WM ASF Writer (QASF)</span></span>](configuring-the-wm-asf-writer--qasf.md)                                   | <span data-ttu-id="15b84-123">Décrit comment configurer le filtre d’enregistreur ASF WM.</span><span class="sxs-lookup"><span data-stu-id="15b84-123">Describes how to configure the WM ASF Writer filter.</span></span>                                   |
| [<span data-ttu-id="15b84-124">Création de graphiques de filtre pour écrire des fichiers ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="15b84-124">Building Filter Graphs to Write ASF Files (QASF)</span></span>](building-filter-graphs-to-write-asf-files--qasf.md)           | <span data-ttu-id="15b84-125">Décrit comment créer des graphiques de transcodage et de capture de fichiers.</span><span class="sxs-lookup"><span data-stu-id="15b84-125">Describes how to create file-transcoding and capture graphs.</span></span>                           |
| [<span data-ttu-id="15b84-126">Configuration des profils et des autres propriétés de fichier (QASF)</span><span class="sxs-lookup"><span data-stu-id="15b84-126">Configuring Profiles and Other File Properties (QASF)</span></span>](configuring-profiles-and-other-file-properties--qasf.md) | <span data-ttu-id="15b84-127">Décrit comment effectuer diverses tâches de configuration de fichiers ASF à l’aide du writer WM ASF.</span><span class="sxs-lookup"><span data-stu-id="15b84-127">Describes how to perform various ASF file-configuration tasks using the WM ASF Writer.</span></span> |



 

 

 
