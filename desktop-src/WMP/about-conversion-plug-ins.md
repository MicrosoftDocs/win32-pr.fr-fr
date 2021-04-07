---
title: À propos des plug-ins de conversion
description: À propos des plug-ins de conversion
ms.assetid: bd6d1020-e8e1-492e-9c76-9f3cf04190de
keywords:
- Lecteur Windows Media, plug-ins de conversion
- Plug-ins du lecteur Windows Media, conversion
- plug-ins, conversion
- plug-ins de conversion, à propos de
- ASF (Advanced Systems Format)
- ASF (format avancé des systèmes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada6e2a8fa41b657a593dc03082f871503b53eba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671569"
---
# <a name="about-conversion-plug-ins"></a><span data-ttu-id="2555a-109">À propos des plug-ins de conversion</span><span class="sxs-lookup"><span data-stu-id="2555a-109">About Conversion Plug-ins</span></span>

<span data-ttu-id="2555a-110">Vous pouvez créer un plug-in de lecteur Windows Media pour convertir des fichiers multimédias numériques créés à l’aide de technologies non fournies par Microsoft, au format ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="2555a-110">You can create a Windows Media Player plug-in to convert digital media files that are created using technologies not provided by Microsoft, into Advanced Systems Format (ASF).</span></span>

<span data-ttu-id="2555a-111">Les plug-ins de conversion sont des objets COM (Component Object Model) qui sont empaquetés et distribués en tant que fichiers exécutables (. exe).</span><span class="sxs-lookup"><span data-stu-id="2555a-111">Conversion plug-ins are Component Object Model (COM) objects that are packaged and distributed as executable (.exe) files.</span></span> <span data-ttu-id="2555a-112">Le lecteur Windows Media instancie les plug-ins de conversion pour convertir des formats multimédias numériques tiers dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="2555a-112">Windows Media Player instantiates conversion plug-ins to convert third-party digital media formats in the following scenarios:</span></span>

-   <span data-ttu-id="2555a-113">Le contenu multimédia numérique est copié sur l’ordinateur à partir d’un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="2555a-113">Digital media content is copied to the computer from a portable device.</span></span>
-   <span data-ttu-id="2555a-114">Le contenu multimédia numérique est ajouté à la bibliothèque à l’aide de **IWMPMediaCollection :: Add**.</span><span class="sxs-lookup"><span data-stu-id="2555a-114">Digital media content is added to the library by using **IWMPMediaCollection::add**.</span></span>
-   <span data-ttu-id="2555a-115">Le contenu multimédia numérique est ajouté à la bibliothèque à l’aide de la fonctionnalité de recherche du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2555a-115">Digital media content is added to the library by using the search feature of Windows Media Player.</span></span>
-   <span data-ttu-id="2555a-116">Le contenu multimédia numérique est ajouté à la bibliothèque par la fonctionnalité de surveillance des dossiers du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2555a-116">Digital media content is added to the library by the folder monitoring feature of Windows Media Player.</span></span>
-   <span data-ttu-id="2555a-117">Le contenu multimédia numérique est ajouté à la liste de synchronisation lorsque l’utilisateur fait glisser et supprime un fichier.</span><span class="sxs-lookup"><span data-stu-id="2555a-117">Digital media content is added to the sync list when the user drags and drops a file.</span></span>

<span data-ttu-id="2555a-118">Une fois que le lecteur Windows Media a créé une instance d’un plug-in de conversion, le plug-in doit convertir le fichier fourni en ASF ou WMA et ajouter les métadonnées appropriées.</span><span class="sxs-lookup"><span data-stu-id="2555a-118">After Windows Media Player creates an instance of a conversion plug-in, the plug-in must convert the supplied file to ASF or WMA and add relevant metadata.</span></span> <span data-ttu-id="2555a-119">(N’utilisez pas le plug-in de conversion pour Transcoder le fichier.) Le plug-in doit ensuite copier le fichier converti dans le dossier spécifié et retourner le chemin d’accès au nouveau fichier dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2555a-119">(Do not use the conversion plug-in to transcode the file.) The plug-in must then copy the converted file to the specified folder and return the path to the new file to Windows Media Player.</span></span>

<span data-ttu-id="2555a-120">Les plug-ins de conversion doivent implémenter l’interface **IWMPConvert** .</span><span class="sxs-lookup"><span data-stu-id="2555a-120">Conversion plug-ins must implement the **IWMPConvert** interface.</span></span> <span data-ttu-id="2555a-121">Consultez [les informations de référence sur la programmation de plug-ins de conversion](conversion-plug-ins-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="2555a-121">See [Conversion Plug-ins Programming Reference](conversion-plug-ins-programming-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2555a-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2555a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2555a-123">**À propos du processus de conversion**</span><span class="sxs-lookup"><span data-stu-id="2555a-123">**About the Conversion Process**</span></span>](about-the-conversion-process.md)
</dt> <dt>

[<span data-ttu-id="2555a-124">**Ajout de métadonnées aux fichiers convertis**</span><span class="sxs-lookup"><span data-stu-id="2555a-124">**Adding Metadata to Converted Files**</span></span>](adding-metadata-to-converted-files.md)
</dt> <dt>

[<span data-ttu-id="2555a-125">**Plug-ins de conversion du lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="2555a-125">**Windows Media Player Conversion Plug-ins**</span></span>](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




