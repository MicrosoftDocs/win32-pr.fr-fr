---
description: Cette section décrit comment utiliser l’API de document XPS pour effectuer des tâches de programmation.
ms.assetid: 05b3d7b6-7628-4a5f-87b7-9d51ead51c79
title: Utilisation de l’API de document XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8870c64bfa8fe478fb71174703c82a96e3723c53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952836"
---
# <a name="using-xps-document-api"></a><span data-ttu-id="2913c-103">Utilisation de l’API de document XPS</span><span class="sxs-lookup"><span data-stu-id="2913c-103">Using XPS Document API</span></span>

<span data-ttu-id="2913c-104">Cette section décrit comment utiliser l' [API de document XPS](documents-xps.md) pour effectuer des tâches de programmation.</span><span class="sxs-lookup"><span data-stu-id="2913c-104">This section describes how to use the [XPS Document API](documents-xps.md) to perform programming tasks.</span></span>

<span data-ttu-id="2913c-105">Pour obtenir des exemples d’utilisation de l' [API de document XPS](documents-xps.md) dans un programme, consultez la section tâches de programmation de l' [API de document XPS](#xps-document-api-programming-tasks) .</span><span class="sxs-lookup"><span data-stu-id="2913c-105">For examples of how to use the [XPS Document API](documents-xps.md) in a program, see the [XPS Document API Programming Tasks](#xps-document-api-programming-tasks) section.</span></span>

<span data-ttu-id="2913c-106">Pour plus d’informations sur l’utilisation du modèle d’objet XPS et sur son implémentation par l' [API de document XPS](documents-xps.md), consultez [à propos de l’API de document XPS](about-xps-document-api.md).</span><span class="sxs-lookup"><span data-stu-id="2913c-106">For information about how to use the XPS Object Model and how it is implemented by the [XPS Document API](documents-xps.md), see [About XPS Document API](about-xps-document-api.md).</span></span>

## <a name="getting-started-with-the-xps-document-api"></a><span data-ttu-id="2913c-107">Prise en main avec l’API de document XPS</span><span class="sxs-lookup"><span data-stu-id="2913c-107">Getting Started with the XPS Document API</span></span>

<span data-ttu-id="2913c-108">Avant de commencer à utiliser l’API de document XPS, assurez-vous que vous êtes familiarisé avec les rubriques de programmation suivantes :</span><span class="sxs-lookup"><span data-stu-id="2913c-108">Before you start using the XPS Document API, make sure that you are familiar with the following programming topics:</span></span><dl>

[<span data-ttu-id="2913c-109">Programmation COM</span><span class="sxs-lookup"><span data-stu-id="2913c-109">COM Programming</span></span>](/windows/desktop/com/component-object-model--com--portal)  
[<span data-ttu-id="2913c-110">Gestion des erreurs dans COM</span><span class="sxs-lookup"><span data-stu-id="2913c-110">Error Handling in COM</span></span>](/windows/desktop/com/error-handling-in-com)  
</dl>

<span data-ttu-id="2913c-111">Lorsque vous utilisez l’API de document XPS, vous pouvez également utiliser les technologies suivantes :</span><span class="sxs-lookup"><span data-stu-id="2913c-111">When using the XPS Document API, you might also want to use the following technologies:</span></span><dl>

[<span data-ttu-id="2913c-112">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="2913c-112">DirectWrite</span></span>](/windows/desktop/DirectWrite/direct-write-portal)  
[<span data-ttu-id="2913c-113">API d’impression XPS</span><span class="sxs-lookup"><span data-stu-id="2913c-113">XPS Print API</span></span>](./printing-with-the-xpsprint-api.md)  
[<span data-ttu-id="2913c-114">API de signature numérique XPS</span><span class="sxs-lookup"><span data-stu-id="2913c-114">XPS Digital Signature API</span></span>](xps-digital-signatures.md)  
</dl>

## <a name="xps-document-api-programming-tasks"></a><span data-ttu-id="2913c-115">Tâches de programmation de l’API de document XPS</span><span class="sxs-lookup"><span data-stu-id="2913c-115">XPS Document API Programming Tasks</span></span>

<span data-ttu-id="2913c-116">Les rubriques de cette section décrivent l’utilisation de l' [API de document XPS](documents-xps.md) dans un programme et montrent comment effectuer des tâches de programmation courantes.</span><span class="sxs-lookup"><span data-stu-id="2913c-116">The topics in this section describe how to use the [XPS Document API](documents-xps.md) in a program and demonstrate how to perform some common programming tasks.</span></span>

<span data-ttu-id="2913c-117">L’API de document XPS utilise des collections pour travailler avec des groupes d’interfaces.</span><span class="sxs-lookup"><span data-stu-id="2913c-117">The XPS Document API uses collections to work with groups of interfaces.</span></span> <span data-ttu-id="2913c-118">[Utilisation des interfaces de collection XPS OM](working-with-xps-object-model-collection-interfaces.md) décrit comment programmer avec ces collections.</span><span class="sxs-lookup"><span data-stu-id="2913c-118">[Working with XPS OM Collection Interfaces](working-with-xps-object-model-collection-interfaces.md) describes how to program with these collections.</span></span>

<span data-ttu-id="2913c-119">Les [tâches courantes de programmation de documents XPS](common-xps-document-tasks.md) sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2913c-119">The [Common XPS Document Programming Tasks](common-xps-document-tasks.md) include the following:</span></span>

<dl>

[<span data-ttu-id="2913c-120">Initialiser un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="2913c-120">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)  
[<span data-ttu-id="2913c-121">Créer un modèle d’objet XPS vide</span><span class="sxs-lookup"><span data-stu-id="2913c-121">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)  
[<span data-ttu-id="2913c-122">Lire un document XPS dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="2913c-122">Read an XPS Document into an XPS OM</span></span>](read-an-xps-document-into-an-xps-om.md)  
[<span data-ttu-id="2913c-123">Naviguer dans le modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="2913c-123">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)  
[<span data-ttu-id="2913c-124">Écrire du texte dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="2913c-124">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)  
[<span data-ttu-id="2913c-125">Dessiner des graphiques dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="2913c-125">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)  
[<span data-ttu-id="2913c-126">Placer des images dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="2913c-126">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)  
[<span data-ttu-id="2913c-127">Écrire un modèle OM XPS dans un document XPS</span><span class="sxs-lookup"><span data-stu-id="2913c-127">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)  
[<span data-ttu-id="2913c-128">Imprimer un modèle OM XPS</span><span class="sxs-lookup"><span data-stu-id="2913c-128">Print an XPS OM</span></span>](print-an-xps-om.md)  
  
</dl>

<span data-ttu-id="2913c-129">Les [tâches de programmation de documents XPS avancées](advanced-xps-document-tasks.md) sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2913c-129">The [Advanced XPS Document Programming Tasks](advanced-xps-document-tasks.md) include the following:</span></span>

<dl>

[<span data-ttu-id="2913c-130">Fusionner les documents XPS</span><span class="sxs-lookup"><span data-stu-id="2913c-130">Merge XPS Documents</span></span>](merging-xps-documents.md)  
[<span data-ttu-id="2913c-131">Traitement de documents XPS dans un filtre XPSDrv</span><span class="sxs-lookup"><span data-stu-id="2913c-131">Processing XPS Documents in an XPSDrv Filter</span></span>](processing-xps-documents-in-an-xpsdrv-filter.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="2913c-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2913c-132">Related topics</span></span>

<dl> <span data-ttu-id="2913c-133"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="2913c-133"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="2913c-134">Informations de référence sur l’API de document XPS</span><span class="sxs-lookup"><span data-stu-id="2913c-134">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="2913c-135">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="2913c-135">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
