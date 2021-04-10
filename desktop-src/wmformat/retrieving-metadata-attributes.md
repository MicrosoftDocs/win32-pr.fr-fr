---
title: Récupération des attributs de métadonnées
description: Récupération des attributs de métadonnées
ms.assetid: d1d2c8e0-7445-4ee1-94d9-4c1ed74f8fe2
keywords:
- Windows Media Format SDK, récupération des attributs de métadonnées
- ASF (Advanced Systems Format), récupération des attributs de métadonnées
- ASF (format des systèmes avancés), récupération des attributs de métadonnées
- métadonnées, récupérer des attributs
- flux, récupération des attributs de métadonnées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c918cb47e77c3fd69c64de586b84b7f6244e4c9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030768"
---
# <a name="retrieving-metadata-attributes"></a><span data-ttu-id="75229-108">Récupération des attributs de métadonnées</span><span class="sxs-lookup"><span data-stu-id="75229-108">Retrieving Metadata Attributes</span></span>

<span data-ttu-id="75229-109">Pour récupérer un attribut à partir d’un en-tête de fichier, vous devez connaître le numéro de flux et l’index de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="75229-109">To retrieve an attribute from a file header, you must know the stream number and index of the attribute.</span></span> <span data-ttu-id="75229-110">Vous pouvez utiliser la méthode [**IWMHeaderInfo3 :: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) pour obtenir les index de tous les attributs portant le même nom ou tous les index dans la même langue.</span><span class="sxs-lookup"><span data-stu-id="75229-110">You can use the [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) method to get the indexes for all attributes with the same name or all indexes in the same language.</span></span> <span data-ttu-id="75229-111">Comme les autres méthodes de [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), **GetAttributeIndices** traite avec un seul flux, ou avec tous les attributs de niveau fichier à l’aide de Stream 0.</span><span class="sxs-lookup"><span data-stu-id="75229-111">Like the other methods of [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), **GetAttributeIndices** deals with a single stream, or with all file-level attributes using stream 0.</span></span> <span data-ttu-id="75229-112">Vous pouvez utiliser 0xFFFF pour le numéro de flux pour obtenir des index globaux correspondant à vos critères dans tout le fichier, quel que soit le nombre de flux.</span><span class="sxs-lookup"><span data-stu-id="75229-112">You can use 0xFFFF for the stream number to get global indexes matching your criteria throughout the entire file, regardless of stream number.</span></span>

<span data-ttu-id="75229-113">Lorsque vous connaissez l’index de l’attribut que vous souhaitez récupérer, appelez [**IWMHeaderInfo3 :: GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) pour obtenir l’attribut.</span><span class="sxs-lookup"><span data-stu-id="75229-113">When you know the index of the attribute you want to retrieve, call [**IWMHeaderInfo3::GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) to get the attribute.</span></span> <span data-ttu-id="75229-114">Vous devez effectuer deux appels à **GetAttributeByIndexEx** pour chaque attribut récupéré.</span><span class="sxs-lookup"><span data-stu-id="75229-114">You need to make two calls to **GetAttributeByIndexEx** for each attribute retrieved.</span></span> <span data-ttu-id="75229-115">Lors du premier appel, transmettez **null** pour le nom et les pointeurs de tampon de données pour obtenir la taille nécessaire.</span><span class="sxs-lookup"><span data-stu-id="75229-115">On the first call, pass **NULL** for the name and data buffer pointers to get the size needed.</span></span> <span data-ttu-id="75229-116">Allouez ensuite des tampons de la taille indiquée et effectuez le deuxième appel pour récupérer le nom et les données.</span><span class="sxs-lookup"><span data-stu-id="75229-116">Then allocate buffers of the size indicated and make the second call to retrieve the name and data.</span></span>

<span data-ttu-id="75229-117">Pour obtenir un exemple de code illustrant la récupération des attributs de métadonnées, consultez [pour récupérer toutes les métadonnées dans un fichier](to-retrieve-all-metadata-in-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="75229-117">For example code showing how to retrieve metadata attributes, see [To Retrieve All Metadata in a File](to-retrieve-all-metadata-in-a-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="75229-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="75229-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75229-119">**Utilisation des métadonnées**</span><span class="sxs-lookup"><span data-stu-id="75229-119">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




