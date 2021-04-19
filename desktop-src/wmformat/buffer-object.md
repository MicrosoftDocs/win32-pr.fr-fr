---
title: Objet de mémoire tampon
description: Objet de mémoire tampon
ms.assetid: 0812261c-698c-4071-929c-4363a16dd5a8
keywords:
- Windows Media Format SDK, objets de mémoire tampon
- ASF (Advanced Systems Format), objets de mémoire tampon
- ASF (format des systèmes avancés), objets de mémoire tampon
- objets, mémoires tampons
- objets de mémoire tampon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8a9a3c6acfa0b0780b07f2853f60fdd68d0eaf
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "106509641"
---
# <a name="buffer-object"></a><span data-ttu-id="c1eb6-108">Objet de mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="c1eb6-108">Buffer Object</span></span>

<span data-ttu-id="c1eb6-109">Un objet buffer est utilisé pour contenir des exemples et les fournir entre les objets du kit de développement logiciel (SDK) Windows Media format et votre application.</span><span class="sxs-lookup"><span data-stu-id="c1eb6-109">A buffer object is used to hold samples and deliver them between the objects of the Windows Media Format SDK and your application.</span></span> <span data-ttu-id="c1eb6-110">Lorsque vous écrivez un fichier, vous transmettez vos exemples d’entrée au writer à l’aide d’objets de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c1eb6-110">When you write a file, you pass your input samples to the writer using buffer objects.</span></span> <span data-ttu-id="c1eb6-111">Quand vous lisez un fichier, l’objet lecteur ou l’objet lecteur synchrone fournit des exemples à votre application dans les objets buffer.</span><span class="sxs-lookup"><span data-stu-id="c1eb6-111">When you read a file, the reader object or synchronous reader object provides samples to your application in buffer objects.</span></span>

<span data-ttu-id="c1eb6-112">Pour écrire des exemples dans un fichier, vous pouvez créer un objet de mémoire tampon à l’aide de la méthode [**IWMWriter :: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) .</span><span class="sxs-lookup"><span data-stu-id="c1eb6-112">For writing samples to a file, you can create a buffer object using the [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) method.</span></span> <span data-ttu-id="c1eb6-113">Pour la lecture des exemples, l’objet lecteur et l’objet lecteur synchrone créent tous deux des objets de mémoire tampon en interne.</span><span class="sxs-lookup"><span data-stu-id="c1eb6-113">For reading samples, the reader object and synchronous reader object both create buffer objects internally.</span></span> <span data-ttu-id="c1eb6-114">Si vous le souhaitez, vous pouvez allouer vos propres objets de mémoire tampon pour la lecture de fichier à l’aide de [**IWMReaderAllocatorEx :: AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex) ou [**IWMReaderAllocatorEx :: AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span><span class="sxs-lookup"><span data-stu-id="c1eb6-114">If you choose to, you can allocate your own buffer objects for file reading by using [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex) or [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span></span>

<span data-ttu-id="c1eb6-115">Les interfaces suivantes sont prises en charge par chaque objet de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c1eb6-115">The following interfaces are supported by every buffer object.</span></span>



| <span data-ttu-id="c1eb6-116">Interface</span><span class="sxs-lookup"><span data-stu-id="c1eb6-116">Interface</span></span>                          | <span data-ttu-id="c1eb6-117">Description</span><span class="sxs-lookup"><span data-stu-id="c1eb6-117">Description</span></span>                                                          |
|------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="c1eb6-118">**INSSBuffer**</span><span class="sxs-lookup"><span data-stu-id="c1eb6-118">**INSSBuffer**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)   | <span data-ttu-id="c1eb6-119">Contrôle et fournit l’accès à la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c1eb6-119">Controls and provides access to the buffer.</span></span>                          |
| [<span data-ttu-id="c1eb6-120">**INSSBuffer2**</span><span class="sxs-lookup"><span data-stu-id="c1eb6-120">**INSSBuffer2**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer2) | <span data-ttu-id="c1eb6-121">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="c1eb6-121">Not implemented.</span></span>                                                     |
| [<span data-ttu-id="c1eb6-122">**INSSBuffer3**</span><span class="sxs-lookup"><span data-stu-id="c1eb6-122">**INSSBuffer3**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) | <span data-ttu-id="c1eb6-123">Prend en charge les propriétés de mémoire tampon, qui sont utilisées pour les extensions d’unité de données.</span><span class="sxs-lookup"><span data-stu-id="c1eb6-123">Supports buffer properties, which are used for data unit extensions.</span></span> |
| [<span data-ttu-id="c1eb6-124">**INSSBuffer4**</span><span class="sxs-lookup"><span data-stu-id="c1eb6-124">**INSSBuffer4**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) | <span data-ttu-id="c1eb6-125">Énumère les propriétés de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c1eb6-125">Enumerates buffer properties.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="c1eb6-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c1eb6-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1eb6-127">**Objets**</span><span class="sxs-lookup"><span data-stu-id="c1eb6-127">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




