---
description: Cette section contient des informations de référence pour les interfaces COM utilisées pour lire et écrire à partir de fichiers DirectX. x. Action déconseillée.
ms.assetid: 66e3476a-4ee8-48ac-aab8-6653793e0ef3
title: X, interfaces de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6e47325a4912faeb919cb60571de3cccbbe265
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521935"
---
# <a name="x-file-interfaces"></a><span data-ttu-id="65e0d-104">X, interfaces de fichiers</span><span class="sxs-lookup"><span data-stu-id="65e0d-104">X File Interfaces</span></span>

<span data-ttu-id="65e0d-105">Cette section contient des informations de référence pour les interfaces COM utilisées pour lire et écrire à partir de fichiers DirectX. x.</span><span class="sxs-lookup"><span data-stu-id="65e0d-105">This section contains reference information for the COM interfaces used to read to and write from DirectX .x files.</span></span> <span data-ttu-id="65e0d-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="65e0d-106">Deprecated.</span></span>

-   [<span data-ttu-id="65e0d-107">**IDirectXFile**</span><span class="sxs-lookup"><span data-stu-id="65e0d-107">**IDirectXFile**</span></span>](idirectxfile.md)
-   [<span data-ttu-id="65e0d-108">**IDirectXFileBinary**</span><span class="sxs-lookup"><span data-stu-id="65e0d-108">**IDirectXFileBinary**</span></span>](idirectxfilebinary.md)
-   [<span data-ttu-id="65e0d-109">**IDirectXFileData**</span><span class="sxs-lookup"><span data-stu-id="65e0d-109">**IDirectXFileData**</span></span>](idirectxfiledata.md)
-   [<span data-ttu-id="65e0d-110">**IDirectXFileDataReference**</span><span class="sxs-lookup"><span data-stu-id="65e0d-110">**IDirectXFileDataReference**</span></span>](idirectxfiledatareference.md)
-   [<span data-ttu-id="65e0d-111">**IDirectXFileEnumObject**</span><span class="sxs-lookup"><span data-stu-id="65e0d-111">**IDirectXFileEnumObject**</span></span>](idirectxfileenumobject.md)
-   [<span data-ttu-id="65e0d-112">**IDirectXFileObject**</span><span class="sxs-lookup"><span data-stu-id="65e0d-112">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
-   [<span data-ttu-id="65e0d-113">**IDirectXFileSaveObject**</span><span class="sxs-lookup"><span data-stu-id="65e0d-113">**IDirectXFileSaveObject**</span></span>](idirectxfilesaveobject.md)

<span data-ttu-id="65e0d-114">Les tableaux suivants illustrent la relation entre les interfaces de fichier. x.</span><span class="sxs-lookup"><span data-stu-id="65e0d-114">The following tables illustrate the relationship between the .x file interfaces.</span></span>



| <span data-ttu-id="65e0d-115">Interface</span><span class="sxs-lookup"><span data-stu-id="65e0d-115">Interface</span></span>             | <span data-ttu-id="65e0d-116">Dérive de</span><span class="sxs-lookup"><span data-stu-id="65e0d-116">Derives from</span></span>           | <span data-ttu-id="65e0d-117">Dérive de</span><span class="sxs-lookup"><span data-stu-id="65e0d-117">Derives from</span></span> |
|-----------------------|------------------------|--------------|
|                       | <span data-ttu-id="65e0d-118">IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="65e0d-118">IDirectXFile</span></span>           | <span data-ttu-id="65e0d-119">IUnknown</span><span class="sxs-lookup"><span data-stu-id="65e0d-119">IUnknown</span></span>     |
| <span data-ttu-id="65e0d-120">IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="65e0d-120">IDirectXFileBinary</span></span>    | <span data-ttu-id="65e0d-121">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="65e0d-121">IDirectXFileObject</span></span>     | <span data-ttu-id="65e0d-122">IUnknown</span><span class="sxs-lookup"><span data-stu-id="65e0d-122">IUnknown</span></span>     |
| <span data-ttu-id="65e0d-123">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="65e0d-123">IDirectXFileData</span></span>      | <span data-ttu-id="65e0d-124">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="65e0d-124">IDirectXFileObject</span></span>     | <span data-ttu-id="65e0d-125">IUnknown</span><span class="sxs-lookup"><span data-stu-id="65e0d-125">IUnknown</span></span>     |
| <span data-ttu-id="65e0d-126">IDirectXFileReference</span><span class="sxs-lookup"><span data-stu-id="65e0d-126">IDirectXFileReference</span></span> | <span data-ttu-id="65e0d-127">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="65e0d-127">IDirectXFileObject</span></span>     | <span data-ttu-id="65e0d-128">IUnknown</span><span class="sxs-lookup"><span data-stu-id="65e0d-128">IUnknown</span></span>     |
|                       | <span data-ttu-id="65e0d-129">IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="65e0d-129">IDirectXFileSaveObject</span></span> | <span data-ttu-id="65e0d-130">IUnknown</span><span class="sxs-lookup"><span data-stu-id="65e0d-130">IUnknown</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="65e0d-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="65e0d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65e0d-132">Référence de fichier X (héritée)</span><span class="sxs-lookup"><span data-stu-id="65e0d-132">X File Reference (Legacy)</span></span>](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 



