---
title: Pour modifier des métadonnées avec le writer
description: Pour modifier des métadonnées avec le writer
ms.assetid: 86badfe3-64bc-4285-a231-f6c0ebf4f262
keywords:
- Windows Media Format SDK, modification des métadonnées avec le writer
- Windows Media Format SDK, modification des métadonnées
- ASF (Advanced Systems Format), modification des métadonnées avec l’enregistreur
- ASF (format de systèmes avancés), modification des métadonnées avec le writer
- ASF (Advanced Systems Format), modification des métadonnées
- ASF (format de systèmes avancés), modification de métadonnées
- métadonnées, modification avec l’enregistreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2823b266b51da366683ac0b5cf65e10debf1ad
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104381697"
---
# <a name="to-edit-metadata-with-the-writer"></a><span data-ttu-id="05e72-110">Pour modifier des métadonnées avec le writer</span><span class="sxs-lookup"><span data-stu-id="05e72-110">To Edit Metadata with the Writer</span></span>

<span data-ttu-id="05e72-111">Vous pouvez accéder, directement à partir de l’enregistreur, aux métadonnées qui seront placées dans l’en-tête du fichier.</span><span class="sxs-lookup"><span data-stu-id="05e72-111">You can access, directly from the writer, the metadata that will go into the header of the file.</span></span> <span data-ttu-id="05e72-112">Appelez la méthode **QueryInterface** de toute interface dans l’objet Writer pour obtenir un pointeur vers l’interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) ou [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) .</span><span class="sxs-lookup"><span data-stu-id="05e72-112">Call the **QueryInterface** method of any interface in the writer object to obtain a pointer to the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) or [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) interface.</span></span> <span data-ttu-id="05e72-113">Une fois que vous avez un pointeur vers l’interface appropriée, vous pouvez manipuler les métadonnées comme vous le feriez si vous aviez chargé le fichier dans l’objet de l’éditeur de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="05e72-113">After you have a pointer to the appropriate interface, you can manipulate the metadata just as you would if you had loaded the file in the metadata editor object.</span></span> <span data-ttu-id="05e72-114">Pour plus d’informations sur la modification des métadonnées, consultez [utilisation des métadonnées](working-with-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="05e72-114">For more information about editing metadata, see [Working with Metadata](working-with-metadata.md).</span></span>

<span data-ttu-id="05e72-115">Vous devez apporter toutes les modifications aux métadonnées avant d’appeler [**IWMWriter :: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="05e72-115">You must make all changes to the metadata before calling [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

> [!Note]  
> <span data-ttu-id="05e72-116">Si vous définissez des métadonnées pour un fichier, écrivez le fichier, puis préparez l’écriture d’un nouveau fichier sans libérer l’enregistreur, certaines métadonnées qui ont été définies pour le premier fichier resteront définies et seront incluses dans les fichiers suivants.</span><span class="sxs-lookup"><span data-stu-id="05e72-116">If you set metadata for a file, write the file, and then prepare to write a new file without releasing the writer, some metadata that was set for the first file will remain set and will be included with subsequent files.</span></span> <span data-ttu-id="05e72-117">Lors de l’écriture de plusieurs fichiers avec la même instance de l’objet Writer, vous avez deux options : vérifier toutes les métadonnées avant d’écrire chaque fichier, ou uniquement écrire dans les métadonnées du writer qui s’appliquent à tous les fichiers que vous écrivez.</span><span class="sxs-lookup"><span data-stu-id="05e72-117">When writing several files with the same instance of the writer object, you have two options: check all the metadata before writing each file, or only write in the writer metadata that applies to all of the files you are writing.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="05e72-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="05e72-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05e72-119">**Écriture de fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="05e72-119">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




