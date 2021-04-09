---
title: Référence PRI (package Resource indexer)
description: .
ms.assetid: 15f41d83-d729-45e4-a6bb-5f8c6b78293c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b75c0739b4e7673863a21223fbed749c27e65dc4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940993"
---
# <a name="package-resource-indexing-pri-reference"></a><span data-ttu-id="7dbc9-103">Référence PRI (package Resource indexer)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-103">Package resource indexing (PRI) reference</span></span>

<span data-ttu-id="7dbc9-104">Ensemble d’API pour l’utilisation d’un indexeur de ressource.</span><span class="sxs-lookup"><span data-stu-id="7dbc9-104">A set of APIs for working with a resource indexer.</span></span> <span data-ttu-id="7dbc9-105">Un indexeur de ressource est utilisé pour générer des fichiers PRI (package Resource index) pour une application UWP.</span><span class="sxs-lookup"><span data-stu-id="7dbc9-105">A resource indexer is used to generate package resource index (PRI) files for a UWP app.</span></span> <span data-ttu-id="7dbc9-106">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="7dbc9-106">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7dbc9-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="7dbc9-107">In this section</span></span>

<span data-ttu-id="7dbc9-108">**Fonctions**</span><span class="sxs-lookup"><span data-stu-id="7dbc9-108">**Functions**</span></span>

-   <span data-ttu-id="7dbc9-109">[**MrmCreateConfig**](mrmcreateconfig.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-109">[**MrmCreateConfig**](mrmcreateconfig.md) function</span></span>
-   <span data-ttu-id="7dbc9-110">[**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-110">[**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md) function</span></span>
-   <span data-ttu-id="7dbc9-111">[**MrmCreateResourceFile**](mrmcreateresourcefile.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-111">[**MrmCreateResourceFile**](mrmcreateresourcefile.md) function</span></span>
-   <span data-ttu-id="7dbc9-112">[**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-112">[**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) function</span></span>
-   <span data-ttu-id="7dbc9-113">[**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-113">[**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md) function</span></span>
-   <span data-ttu-id="7dbc9-114">[**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-114">[**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md) function</span></span>
-   <span data-ttu-id="7dbc9-115">[**MrmCreateResourceIndexerFromPreviousPriFile**](mrmcreateresourceindexerfrompreviousprifile.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-115">[**MrmCreateResourceIndexerFromPreviousPriFile**](mrmcreateresourceindexerfrompreviousprifile.md) function</span></span>
-   <span data-ttu-id="7dbc9-116">[**MrmCreateResourceIndexerFromPreviousSchemaData**](mrmcreateresourceindexerfrompreviousschemadata.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-116">[**MrmCreateResourceIndexerFromPreviousSchemaData**](mrmcreateresourceindexerfrompreviousschemadata.md) function</span></span>
-   <span data-ttu-id="7dbc9-117">[**MrmCreateResourceIndexerFromPreviousSchemaFile**](mrmcreateresourceindexerfrompreviousschemafile.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-117">[**MrmCreateResourceIndexerFromPreviousSchemaFile**](mrmcreateresourceindexerfrompreviousschemafile.md) function</span></span>
-   <span data-ttu-id="7dbc9-118">[**MrmDestroyIndexerAndMessages**](mrmdestroyindexerandmessages.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-118">[**MrmDestroyIndexerAndMessages**](mrmdestroyindexerandmessages.md) function</span></span>
-   <span data-ttu-id="7dbc9-119">[**MrmDumpPriFile**](mrmdumpprifile.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-119">[**MrmDumpPriFile**](mrmdumpprifile.md) function</span></span>
-   <span data-ttu-id="7dbc9-120">[**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-120">[**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) function</span></span>
-   <span data-ttu-id="7dbc9-121">[**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-121">[**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md) function</span></span>
-   <span data-ttu-id="7dbc9-122">[**MrmFreeMemory**](mrmfreememory.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-122">[**MrmFreeMemory**](mrmfreememory.md) function</span></span>
-   <span data-ttu-id="7dbc9-123">[**MrmIndexEmbeddedData**](mrmindexembeddeddata.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-123">[**MrmIndexEmbeddedData**](mrmindexembeddeddata.md) function</span></span>
-   <span data-ttu-id="7dbc9-124">[**MrmIndexFile**](mrmindexfile.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-124">[**MrmIndexFile**](mrmindexfile.md) function</span></span>
-   <span data-ttu-id="7dbc9-125">[**MrmIndexFileAutoQualifiers**](mrmindexfileautoqualifiers.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-125">[**MrmIndexFileAutoQualifiers**](mrmindexfileautoqualifiers.md) function</span></span>
-   <span data-ttu-id="7dbc9-126">[**MrmIndexResourceContainerAutoQualifiers**](mrmindexresourcecontainerautoqualifiers.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-126">[**MrmIndexResourceContainerAutoQualifiers**](mrmindexresourcecontainerautoqualifiers.md) function</span></span>
-   <span data-ttu-id="7dbc9-127">[**MrmIndexString**](mrmindexstring.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-127">[**MrmIndexString**](mrmindexstring.md) function</span></span>
-   <span data-ttu-id="7dbc9-128">[**MrmPeekResourceIndexerMessages**](mrmpeekresourceindexermessages.md) fonction)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-128">[**MrmPeekResourceIndexerMessages**](mrmpeekresourceindexermessages.md) function</span></span>

<span data-ttu-id="7dbc9-129">**Structures**</span><span class="sxs-lookup"><span data-stu-id="7dbc9-129">**Structures**</span></span>

-   <span data-ttu-id="7dbc9-130">[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) , structure</span><span class="sxs-lookup"><span data-stu-id="7dbc9-130">[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) structure</span></span>
-   <span data-ttu-id="7dbc9-131">[**MrmResourceIndexerMessage**](mrmresourceindexermessage.md) , structure</span><span class="sxs-lookup"><span data-stu-id="7dbc9-131">[**MrmResourceIndexerMessage**](mrmresourceindexermessage.md) structure</span></span>

<span data-ttu-id="7dbc9-132">**Énumérations**</span><span class="sxs-lookup"><span data-stu-id="7dbc9-132">**Enumerations**</span></span>

-   <span data-ttu-id="7dbc9-133">Énumération [**MrmDumpType**](mrmdumptype.md)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-133">[**MrmDumpType**](mrmdumptype.md) enumeration</span></span>
-   <span data-ttu-id="7dbc9-134">Énumération [**MrmPackagingMode**](mrmpackagingmode.md)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-134">[**MrmPackagingMode**](mrmpackagingmode.md) enumeration</span></span>
-   <span data-ttu-id="7dbc9-135">Énumération [**MrmPackagingOptions**](mrmpackagingoptions.md)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-135">[**MrmPackagingOptions**](mrmpackagingoptions.md) enumeration</span></span>
-   <span data-ttu-id="7dbc9-136">Énumération [**MrmPlatformVersion**](mrmplatformversion.md)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-136">[**MrmPlatformVersion**](mrmplatformversion.md) enumeration</span></span>
-   <span data-ttu-id="7dbc9-137">Énumération [**MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md)</span><span class="sxs-lookup"><span data-stu-id="7dbc9-137">[**MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md) enumeration</span></span>

 

 