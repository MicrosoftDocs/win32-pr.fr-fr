---
description: Cette rubrique explique comment utiliser les interfaces de niveau page qui fournissent l’accès au contenu d’une page dans un modèle d’objet XPS.
ms.assetid: 7127ee28-eca9-4e0e-a27a-9051eb105b27
title: Utilisation des interfaces de page OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8350409f2f436cc4ec2293e735c3f020b49bea68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530595"
---
# <a name="working-with-xps-om-page-interfaces"></a><span data-ttu-id="e2171-103">Utilisation des interfaces de page OM XPS</span><span class="sxs-lookup"><span data-stu-id="e2171-103">Working with XPS OM Page Interfaces</span></span>

<span data-ttu-id="e2171-104">Cette rubrique explique comment utiliser les interfaces de niveau page qui fournissent l’accès au contenu d’une page dans un modèle d’objet XPS.</span><span class="sxs-lookup"><span data-stu-id="e2171-104">This topic describes how to use the page-level interfaces that provide access to the contents of a page in an XPS OM.</span></span>



| <span data-ttu-id="e2171-105">Nom de l’interface</span><span class="sxs-lookup"><span data-stu-id="e2171-105">Interface name</span></span>                                                                                                                                                                              | <span data-ttu-id="e2171-106">Interfaces enfants logiques</span><span class="sxs-lookup"><span data-stu-id="e2171-106">Logical child interfaces</span></span>                                                                                                                                                                                            | <span data-ttu-id="e2171-107">Description</span><span class="sxs-lookup"><span data-stu-id="e2171-107">Description</span></span>                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2171-108">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="e2171-108">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                                                                                                                                                 | [<span data-ttu-id="e2171-109">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="e2171-109">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [<span data-ttu-id="e2171-110">**IXpsOMGlyphs**</span><span class="sxs-lookup"><span data-stu-id="e2171-110">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [<span data-ttu-id="e2171-111">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="e2171-111">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                                                                         | <span data-ttu-id="e2171-112">Objet racine du contenu de la page.</span><span class="sxs-lookup"><span data-stu-id="e2171-112">The root object of the page contents.</span></span><br/> <span data-ttu-id="e2171-113">Cet objet représente une partie de document.</span><span class="sxs-lookup"><span data-stu-id="e2171-113">This object represents a document part.</span></span><br/>                                                |
| [<span data-ttu-id="e2171-114">**IXpsOMShareable**</span><span class="sxs-lookup"><span data-stu-id="e2171-114">**IXpsOMShareable**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable)<br/>                                                                                                                                       | [<span data-ttu-id="e2171-115">**IXpsOMVisual**</span><span class="sxs-lookup"><span data-stu-id="e2171-115">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> [<span data-ttu-id="e2171-116">**IXpsOMMatrixTransform**</span><span class="sxs-lookup"><span data-stu-id="e2171-116">**IXpsOMMatrixTransform**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)<br/> [<span data-ttu-id="e2171-117">**IXpsOMGeometry**</span><span class="sxs-lookup"><span data-stu-id="e2171-117">**IXpsOMGeometry**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)<br/> [<span data-ttu-id="e2171-118">**IXpsOMBrush**</span><span class="sxs-lookup"><span data-stu-id="e2171-118">**IXpsOMBrush**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush)<br/> | <span data-ttu-id="e2171-119">Les interfaces qui dérivent de l’interface [**IXpsOMShareable**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable) peuvent être stockées dans un dictionnaire de ressources et partagées.</span><span class="sxs-lookup"><span data-stu-id="e2171-119">Interfaces that derive from the [**IXpsOMShareable**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable) interface can be stored in a resource dictionary and shared.</span></span><br/> |
| [<span data-ttu-id="e2171-120">**IXpsOMRemoteDictionaryResource**</span><span class="sxs-lookup"><span data-stu-id="e2171-120">**IXpsOMRemoteDictionaryResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)<br/> [<span data-ttu-id="e2171-121">**IXpsOMRemoteDictionaryResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="e2171-121">**IXpsOMRemoteDictionaryResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)<br/> | [<span data-ttu-id="e2171-122">**IXpsOMDictionary**</span><span class="sxs-lookup"><span data-stu-id="e2171-122">**IXpsOMDictionary**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                                             | <span data-ttu-id="e2171-123">Contient un dictionnaire de ressources.</span><span class="sxs-lookup"><span data-stu-id="e2171-123">Contains a resource dictionary.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="e2171-124">**IXpsOMDictionary**</span><span class="sxs-lookup"><span data-stu-id="e2171-124">**IXpsOMDictionary**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                     | <span data-ttu-id="e2171-125">Aucun</span><span class="sxs-lookup"><span data-stu-id="e2171-125">None</span></span><br/>                                                                                                                                                                                                     | <span data-ttu-id="e2171-126">Référence les ressources qui sont partagées par d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="e2171-126">References the resources that are shared by other objects.</span></span><br/>                                                                              |
| [<span data-ttu-id="e2171-127">**IXpsOMStoryFragmentsResource**</span><span class="sxs-lookup"><span data-stu-id="e2171-127">**IXpsOMStoryFragmentsResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)<br/>                                                                                                             | <span data-ttu-id="e2171-128">Aucun</span><span class="sxs-lookup"><span data-stu-id="e2171-128">None</span></span><br/>                                                                                                                                                                                                     | <span data-ttu-id="e2171-129">Fournit l’accès au contenu du flux de ressources de la partie StoryFragments du document.</span><span class="sxs-lookup"><span data-stu-id="e2171-129">Provides access to the content of the resource stream of the StoryFragments part of the document.</span></span><br/>                                       |



 

## <a name="related-topics"></a><span data-ttu-id="e2171-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e2171-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2171-131">**Interface IXpsOMDictionary**</span><span class="sxs-lookup"><span data-stu-id="e2171-131">**IXpsOMDictionary Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)
</dt> <dt>

[<span data-ttu-id="e2171-132">**IXpsOMDocumentStructureResource**</span><span class="sxs-lookup"><span data-stu-id="e2171-132">**IXpsOMDocumentStructureResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)
</dt> <dt>

[<span data-ttu-id="e2171-133">**Interface IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="e2171-133">**IXpsOMPage Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="e2171-134">**Interface IXpsOMRemoteDictionaryResource**</span><span class="sxs-lookup"><span data-stu-id="e2171-134">**IXpsOMRemoteDictionaryResource Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)
</dt> <dt>

[<span data-ttu-id="e2171-135">**Interface IXpsOMRemoteDictionaryResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="e2171-135">**IXpsOMRemoteDictionaryResourceCollection Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)
</dt> <dt>

[<span data-ttu-id="e2171-136">**Interface IXpsOMStoryFragmentsResource**</span><span class="sxs-lookup"><span data-stu-id="e2171-136">**IXpsOMStoryFragmentsResource Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)
</dt> </dl>

 

 




