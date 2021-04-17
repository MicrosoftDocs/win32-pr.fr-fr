---
title: Pour configurer l’indexeur
description: Pour configurer l’indexeur
ms.assetid: 0e28e8dd-1586-45e6-8a08-5245d465d068
keywords:
- Windows Media Format SDK, configuration d’indexeurs
- ASF (Advanced Systems Format), configuration des indexeurs
- ASF (format des systèmes avancés), configuration des indexeurs
- index, configuration d’indexeurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618316e22b13ca05ff0fc1bbfb6b4583e79ca858
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381537"
---
# <a name="to-configure-the-indexer"></a><span data-ttu-id="6292b-107">Pour configurer l’indexeur</span><span class="sxs-lookup"><span data-stu-id="6292b-107">To Configure the Indexer</span></span>

<span data-ttu-id="6292b-108">Vous pouvez configurer l’indexeur avant de l’utiliser pour indexer un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="6292b-108">You can configure the indexer before using it to index an ASF file.</span></span> <span data-ttu-id="6292b-109">Chaque flux du fichier peut être configuré séparément, ou vous pouvez définir la même configuration pour tous les flux.</span><span class="sxs-lookup"><span data-stu-id="6292b-109">Each stream in the file can be configured separately, or you can set the same configuration for all streams.</span></span>

<span data-ttu-id="6292b-110">Si vous configurez plusieurs vapeurs pour l’indexation dans un fichier, vous devez les configurer toutes, puis commencer l’indexation.</span><span class="sxs-lookup"><span data-stu-id="6292b-110">If you are configuring multiple steams for indexing in a file, you must configure them all and then begin indexing.</span></span> <span data-ttu-id="6292b-111">Si vous configurez et indexez un flux, puis configurez un autre flux dans le même fichier, le redémarrage de l’indexeur supprimera le premier index.</span><span class="sxs-lookup"><span data-stu-id="6292b-111">If you configure and index a stream and then configure another stream in the same file, starting the indexer again will delete the first index.</span></span> <span data-ttu-id="6292b-112">Cela est conforme au format de fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="6292b-112">This is to comply with the ASF file format.</span></span>

<span data-ttu-id="6292b-113">Le code suivant montre comment configurer l’indexeur.</span><span class="sxs-lookup"><span data-stu-id="6292b-113">The following code shows how to configure the indexer.</span></span> <span data-ttu-id="6292b-114">Le code suppose que le fichier à indexer a deux flux : le premier est un flux audio qui n’a pas besoin d’être indexé et le second est un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="6292b-114">The code assumes that the file to be indexed has two streams: the first is an audio stream which does not need to be indexed, and the second is a video stream.</span></span> <span data-ttu-id="6292b-115">Ce code illustre uniquement la configuration de l’indexeur.</span><span class="sxs-lookup"><span data-stu-id="6292b-115">This code shows only how to configure the indexer.</span></span> <span data-ttu-id="6292b-116">Pour indexer un fichier, vous devez suivre les étapes présentées dans [pour indexer un fichier ASF](to-index-an-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="6292b-116">To index a file, you must follow the steps presented in [To Index an ASF File](to-index-an-asf-file.md).</span></span>


```C++
IWMIndexer*  pBaseIndexer = NULL;
IWMIndexer2* pMyIndexer   = NULL;

DWORD          dwInterval;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create an indexer.
hr = WMCreateIndexer(&pBaseIndexer);

// Retrieve an IWMIndexer2 interface pointer for the indexer just created.
hr = pBaseIndexer->QueryInterface(IID_IWMIndexer2, (void**)&pMyIndexer);

// Release the base indexer.
pBaseIndexer->Release();
pBaseIndexer = NULL;

// Set the index interval to 5 frames.
dwInterval = 5;

// Configure the indexer to create a frame-based index.
hr = pMyIndexer->Configure(2,                    // Stream Number.
                           WMT_IT_FRAME_NUMBERS, // Indexer type.
                           (void *)&dwInterval,  // Index interval.
                           NULL;        // Index type, use default.

// TODO: Index the file. See To Index an ASF File.

// Release the remaining interface.
pMyIndexer->Release();
pMyIndexer = NULL;

```



> [!Note]  
> <span data-ttu-id="6292b-117">Le type d’index par défaut est le \_ \_ point de nettoyage le plus proche de WMT \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6292b-117">The default index type is WMT\_IT\_NEAREST\_CLEAN\_POINT.</span></span> <span data-ttu-id="6292b-118">Bien que vous puissiez définir le type d’index sur d’autres valeurs, cela dégradera les performances de recherche.</span><span class="sxs-lookup"><span data-stu-id="6292b-118">Although you can set the index type to other values, doing so will degrade seeking performance.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6292b-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6292b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6292b-120">**IWMIndexer2 :: configure**</span><span class="sxs-lookup"><span data-stu-id="6292b-120">**IWMIndexer2::Configure**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure)
</dt> <dt>

[<span data-ttu-id="6292b-121">**Pour indexer un fichier ASF**</span><span class="sxs-lookup"><span data-stu-id="6292b-121">**To Index an ASF File**</span></span>](to-index-an-asf-file.md)
</dt> <dt>

[<span data-ttu-id="6292b-122">**WMCreateIndexer**</span><span class="sxs-lookup"><span data-stu-id="6292b-122">**WMCreateIndexer**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[<span data-ttu-id="6292b-123">**Utilisation des index**</span><span class="sxs-lookup"><span data-stu-id="6292b-123">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




