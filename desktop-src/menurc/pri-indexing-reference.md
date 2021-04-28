---
title: Référence PRI (package Resource indexer)
description: Référence PRI (package Resource indexer)
ms.assetid: 15f41d83-d729-45e4-a6bb-5f8c6b78293c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef99acafe4fbdadef26c5947145ad734ec44b7bd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117547"
---
# <a name="package-resource-indexing-pri-reference"></a><span data-ttu-id="24a94-103">Référence PRI (package Resource indexer)</span><span class="sxs-lookup"><span data-stu-id="24a94-103">Package resource indexing (PRI) reference</span></span>

<span data-ttu-id="24a94-104">Ensemble d’API pour l’utilisation d’un indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="24a94-104">A set of APIs for working with a resource indexer.</span></span> <span data-ttu-id="24a94-105">Un indexeur de ressource est utilisé pour générer des fichiers PRI (package Resource index) pour une application UWP.</span><span class="sxs-lookup"><span data-stu-id="24a94-105">A resource indexer is used to generate package resource index (PRI) files for a UWP app.</span></span> <span data-ttu-id="24a94-106">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="24a94-106">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="24a94-107">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="24a94-107">In this section</span></span>

<span data-ttu-id="24a94-108">**Fonctions**</span><span class="sxs-lookup"><span data-stu-id="24a94-108">**Functions**</span></span>

-   <span data-ttu-id="24a94-109">[**MrmCreateConfig**](mrmcreateconfig.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="24a94-109">[**MrmCreateConfig**](mrmcreateconfig.md) function</span></span>
-   <span data-ttu-id="24a94-110">[**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="24a94-110">[**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md) function</span></span>
-   <span data-ttu-id="24a94-111">[**MrmCreateResourceFile**](mrmcreateresourcefile.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="24a94-111">[**MrmCreateResourceFile**](mrmcreateresourcefile.md) function</span></span>
-   <span data-ttu-id="24a94-112">[**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="24a94-112">[**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) function</span></span>
-   <span data-ttu-id="24a94-113">[**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="24a94-113">[**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md) function</span></span>
-   <span data-ttu-id="24a94-114">[**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="24a94-114">[**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md) function</span></span>
-   <span data-ttu-id="24a94-115">[**MrmCreateResourceIndexerFromPreviousPriFile**](mrmcreateresourceindexerfrompreviousprifile.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="24a94-115">[**MrmCreateResourceIndexerFromPreviousPriFile**](mrmcreateresourceindexerfrompreviousprifile.md) function</span></span>
-   <span data-ttu-id="24a94-116">[**MrmCreateResourceIndexerFromPreviousSchemaData**](mrmcreateresourceindexerfrompreviousschemadata.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="24a94-116">[**MrmCreateResourceIndexerFromPreviousSchemaData**](mrmcreateresourceindexerfrompreviousschemadata.md) function</span></span>
-   <span data-ttu-id="24a94-117">[**MrmCreateResourceIndexerFromPreviousSchemaFile**](mrmcreateresourceindexerfrompreviousschemafile.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="24a94-117">[**MrmCreateResourceIndexerFromPreviousSchemaFile**](mrmcreateresourceindexerfrompreviousschemafile.md) function</span></span>
-   <span data-ttu-id="24a94-118">[**MrmDestroyIndexerAndMessages**](mrmdestroyindexerandmessages.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="24a94-118">[**MrmDestroyIndexerAndMessages**](mrmdestroyindexerandmessages.md) function</span></span>
-   <span data-ttu-id="24a94-119">[**MrmDumpPriFile**](mrmdumpprifile.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="24a94-119">[**MrmDumpPriFile**](mrmdumpprifile.md) function</span></span>
-   <span data-ttu-id="24a94-120">[**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="24a94-120">[**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) function</span></span>
-   <span data-ttu-id="24a94-121">[**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="24a94-121">[**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md) function</span></span>
-   <span data-ttu-id="24a94-122">[**MrmFreeMemory**](mrmfreememory.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="24a94-122">[**MrmFreeMemory**](mrmfreememory.md) function</span></span>
-   <span data-ttu-id="24a94-123">[**MrmIndexEmbeddedData**](mrmindexembeddeddata.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="24a94-123">[**MrmIndexEmbeddedData**](mrmindexembeddeddata.md) function</span></span>
-   <span data-ttu-id="24a94-124">[**MrmIndexFile**](mrmindexfile.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="24a94-124">[**MrmIndexFile**](mrmindexfile.md) function</span></span>
-   <span data-ttu-id="24a94-125">[**MrmIndexFileAutoQualifiers**](mrmindexfileautoqualifiers.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="24a94-125">[**MrmIndexFileAutoQualifiers**](mrmindexfileautoqualifiers.md) function</span></span>
-   <span data-ttu-id="24a94-126">[**MrmIndexResourceContainerAutoQualifiers**](mrmindexresourcecontainerautoqualifiers.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="24a94-126">[**MrmIndexResourceContainerAutoQualifiers**](mrmindexresourcecontainerautoqualifiers.md) function</span></span>
-   <span data-ttu-id="24a94-127">[**MrmIndexString**](mrmindexstring.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="24a94-127">[**MrmIndexString**](mrmindexstring.md) function</span></span>
-   <span data-ttu-id="24a94-128">[**MrmPeekResourceIndexerMessages**](mrmpeekresourceindexermessages.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="24a94-128">[**MrmPeekResourceIndexerMessages**](mrmpeekresourceindexermessages.md) function</span></span>

<span data-ttu-id="24a94-129">**Structures**</span><span class="sxs-lookup"><span data-stu-id="24a94-129">**Structures**</span></span>

-   <span data-ttu-id="24a94-130">[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) , structure</span><span class="sxs-lookup"><span data-stu-id="24a94-130">[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) structure</span></span>
-   <span data-ttu-id="24a94-131">[**MrmResourceIndexerMessage**](mrmresourceindexermessage.md) , structure</span><span class="sxs-lookup"><span data-stu-id="24a94-131">[**MrmResourceIndexerMessage**](mrmresourceindexermessage.md) structure</span></span>

<span data-ttu-id="24a94-132">**Énumérations**</span><span class="sxs-lookup"><span data-stu-id="24a94-132">**Enumerations**</span></span>

-   <span data-ttu-id="24a94-133">Énumération [**MrmDumpType**](mrmdumptype.md)</span><span class="sxs-lookup"><span data-stu-id="24a94-133">[**MrmDumpType**](mrmdumptype.md) enumeration</span></span>
-   <span data-ttu-id="24a94-134">Énumération [**MrmPackagingMode**](mrmpackagingmode.md)</span><span class="sxs-lookup"><span data-stu-id="24a94-134">[**MrmPackagingMode**](mrmpackagingmode.md) enumeration</span></span>
-   <span data-ttu-id="24a94-135">Énumération [**MrmPackagingOptions**](mrmpackagingoptions.md)</span><span class="sxs-lookup"><span data-stu-id="24a94-135">[**MrmPackagingOptions**](mrmpackagingoptions.md) enumeration</span></span>
-   <span data-ttu-id="24a94-136">Énumération [**MrmPlatformVersion**](mrmplatformversion.md)</span><span class="sxs-lookup"><span data-stu-id="24a94-136">[**MrmPlatformVersion**](mrmplatformversion.md) enumeration</span></span>
-   <span data-ttu-id="24a94-137">Énumération [**MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md)</span><span class="sxs-lookup"><span data-stu-id="24a94-137">[**MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md) enumeration</span></span>

 

 
