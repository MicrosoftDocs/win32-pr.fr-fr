---
title: Types perçus (fonctionnalités héritées de l’environnement Windows)
description: PerceivedType est une propriété qui classifie un élément dans l’index.
ms.assetid: 47a5cf55-79f6-48e7-a585-72fc3d7d53d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afaf7d8b827495a94b441e5504762dd53dbe733c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106518053"
---
# <a name="perceived-types-legacy-windows-environment-features"></a><span data-ttu-id="37414-103">Types perçus (fonctionnalités héritées de l’environnement Windows)</span><span class="sxs-lookup"><span data-stu-id="37414-103">Perceived Types (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="37414-104">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="37414-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="37414-105">Dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="37414-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="37414-106">`PerceivedType` est une propriété qui classifie un élément dans l’index.</span><span class="sxs-lookup"><span data-stu-id="37414-106">`PerceivedType` is a property that classifies an item in the index.</span></span> <span data-ttu-id="37414-107">Cette classification est différente de la classification « Kind » utilisée par la [syntaxe de requête avancée](-search-2x-wds-aqsreference.md) , mais elle permet aux utilisateurs d’affiner leurs résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="37414-107">This classification is different from the "kind" classification used by the [Advanced Query Syntax](-search-2x-wds-aqsreference.md) but similarly lets users refine their search results.</span></span> <span data-ttu-id="37414-108">Le type AQS permet aux utilisateurs de limiter leur requête de recherche, tandis que la propriété PerceivedType permet aux utilisateurs de filtrer leur jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="37414-108">The AQS kind lets users limit their search query while the PerceivedType property lets users filter their result set.</span></span>

## <a name="types"></a><span data-ttu-id="37414-109">Types</span><span class="sxs-lookup"><span data-stu-id="37414-109">Types</span></span>

<span data-ttu-id="37414-110">Utilisez la propriété PerceivedType pour classer votre type de fichier afin que les utilisateurs puissent filtrer leurs résultats de recherche par type.</span><span class="sxs-lookup"><span data-stu-id="37414-110">Use the PerceivedType property to classify your file type so that users can filter their search results by type.</span></span> <span data-ttu-id="37414-111">La sortie doit être l’une des chaînes suivantes :</span><span class="sxs-lookup"><span data-stu-id="37414-111">The output must be one of the following strings:</span></span>

-   <span data-ttu-id="37414-112">contact</span><span class="sxs-lookup"><span data-stu-id="37414-112">contact</span></span>
-   <span data-ttu-id="37414-113">communications</span><span class="sxs-lookup"><span data-stu-id="37414-113">communications</span></span>
-   <span data-ttu-id="37414-114">Communications/courrier électronique</span><span class="sxs-lookup"><span data-stu-id="37414-114">communications/email</span></span>
-   <span data-ttu-id="37414-115">Communications/calendrier</span><span class="sxs-lookup"><span data-stu-id="37414-115">communications/calendar</span></span>
-   <span data-ttu-id="37414-116">Communications/tâche</span><span class="sxs-lookup"><span data-stu-id="37414-116">communications/task</span></span>
-   <span data-ttu-id="37414-117">Communications/messagerie instantanée</span><span class="sxs-lookup"><span data-stu-id="37414-117">communications/im</span></span>
-   <span data-ttu-id="37414-118">document</span><span class="sxs-lookup"><span data-stu-id="37414-118">document</span></span>
-   <span data-ttu-id="37414-119">document/Remarque</span><span class="sxs-lookup"><span data-stu-id="37414-119">document/note</span></span>
-   <span data-ttu-id="37414-120">document/texte</span><span class="sxs-lookup"><span data-stu-id="37414-120">document/text</span></span>
-   <span data-ttu-id="37414-121">document/feuille de calcul</span><span class="sxs-lookup"><span data-stu-id="37414-121">document/spreadsheet</span></span>
-   <span data-ttu-id="37414-122">document/présentation</span><span class="sxs-lookup"><span data-stu-id="37414-122">document/presentation</span></span>
-   <span data-ttu-id="37414-123">music</span><span class="sxs-lookup"><span data-stu-id="37414-123">music</span></span>
-   <span data-ttu-id="37414-124">images</span><span class="sxs-lookup"><span data-stu-id="37414-124">images</span></span>
-   <span data-ttu-id="37414-125">images/image</span><span class="sxs-lookup"><span data-stu-id="37414-125">images/picture</span></span>
-   <span data-ttu-id="37414-126">images/vidéo</span><span class="sxs-lookup"><span data-stu-id="37414-126">images/video</span></span>
-   <span data-ttu-id="37414-127">dossier</span><span class="sxs-lookup"><span data-stu-id="37414-127">folder</span></span>
-   <span data-ttu-id="37414-128">programme</span><span class="sxs-lookup"><span data-stu-id="37414-128">program</span></span>

<span data-ttu-id="37414-129">Par exemple, lorsque vous souhaitez créer un complément de filtre pour un nouveau type de fichier image, vous devez implémenter les éléments suivants dans votre interface [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter):</span><span class="sxs-lookup"><span data-stu-id="37414-129">For example, when you want to create a filter add-in for a new picture file type, you need to implement the following in your [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface:</span></span>

-   <span data-ttu-id="37414-130">**GetChunk** pour retourner un FULLPROPSPEC qui comprend : D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType</span><span class="sxs-lookup"><span data-stu-id="37414-130">**GetChunk** to return a FULLPROPSPEC that includes: D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType</span></span>
-   <span data-ttu-id="37414-131">**GetValue** pour retourner un PROPVARIANT qui comprend : VT \_ LPWStr = "images/image"</span><span class="sxs-lookup"><span data-stu-id="37414-131">**GetValue** to return a PROPVARIANT that includes: VT\_LPWSTR = "images/picture"</span></span>

## <a name="related-topics"></a><span data-ttu-id="37414-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="37414-132">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="37414-133">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="37414-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="37414-134">Développement de compléments IFilter</span><span class="sxs-lookup"><span data-stu-id="37414-134">Developing IFilter Add-ins</span></span>](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[<span data-ttu-id="37414-135">Développement de gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="37414-135">Developing Protocol Handlers</span></span>](-search-2x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="37414-136">Syntaxe de requête avancée</span><span class="sxs-lookup"><span data-stu-id="37414-136">Advanced Query Syntax</span></span>](-search-2x-wds-aqsreference.md)
</dt> <dt>

[<span data-ttu-id="37414-137">SchemaTable</span><span class="sxs-lookup"><span data-stu-id="37414-137">SchemaTable</span></span>](-search-2x-wds-schematable.md)
</dt> </dl>

 

 
