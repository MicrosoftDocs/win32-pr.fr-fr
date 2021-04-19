---
description: L’API de document XPS implémente le modèle d’objet XPS et permet aux développeurs de créer un modèle d’objet XPS, de manipuler le contenu d’un document XPS dans des programmes Windows natifs \\ \\ et d’enregistrer le modèle d’objet XPS dans un fichier ou un flux de données en tant que document XPS.
ms.assetid: dbb48dae-1ee6-4a8b-9184-8b796755087e
title: À propos de l’API de document XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e24a93061b7f09697a987aa83be121dac42703c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536564"
---
# <a name="about-xps-document-api"></a><span data-ttu-id="32257-103">À propos de l’API de document XPS</span><span class="sxs-lookup"><span data-stu-id="32257-103">About XPS Document API</span></span>

<span data-ttu-id="32257-104">L' [API de document XPS](documents-xps.md) implémente le modèle d’objet XPS et permet aux développeurs de créer un modèle d’objet XPS, de manipuler le contenu d’un document XPS dans des programmes Windows natifs \\ \\ et d’enregistrer le modèle d’objet XPS dans un fichier ou un flux de données en tant que document XPS.</span><span class="sxs-lookup"><span data-stu-id="32257-104">The [XPS Document API](documents-xps.md) implements the XPS object model and enables developers to create an XPS OM, manipulate XPS document content in native Windows \\\\ programs, and save the XPS OM to a file or stream as an XPS document.</span></span> <span data-ttu-id="32257-105">Les développeurs de modules de pipeline de filtre XPSDrv peuvent également utiliser l’API de document XPS pour manipuler le contenu d’un document XPS dans un filtre de pilote d’imprimante XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="32257-105">Developers of XPSDrv filter pipeline modules can also use the XPS Document API to manipulate XPS document content in an XPSDrv printer driver filter.</span></span>

## <a name="xps-document-api-overview"></a><span data-ttu-id="32257-106">Vue d’ensemble de l’API de document XPS</span><span class="sxs-lookup"><span data-stu-id="32257-106">XPS Document API Overview</span></span>

<span data-ttu-id="32257-107">Le modèle objet XPS est le modèle d’informations d’un document XPS.</span><span class="sxs-lookup"><span data-stu-id="32257-107">The XPS object model is the information model of an XPS document.</span></span> <span data-ttu-id="32257-108">Le modèle d’information du document XPS est distinct du modèle de balisage utilisé à l’intérieur des parties du document.</span><span class="sxs-lookup"><span data-stu-id="32257-108">The information model of the XPS document is separate from the markup model that is used inside the document parts.</span></span> <span data-ttu-id="32257-109">Le modèle d’objet XPS décrit l’Organisation des composants internes qui composent un document XPS, et le modèle de balisage décrit le contenu de ces composants.</span><span class="sxs-lookup"><span data-stu-id="32257-109">The XPS object model describes the organization of the internal components that make up an XPS document, and the markup model describes the contents of those components.</span></span>

<span data-ttu-id="32257-110">Dans un programme, le modèle objet XPS est instancié comme un modèle d’objet XPS.</span><span class="sxs-lookup"><span data-stu-id="32257-110">In a program, the XPS object model is instantiated as an XPS OM.</span></span> <span data-ttu-id="32257-111">Le modèle d’objet XPS est essentiellement une version en mémoire du contenu d’un document XPS.</span><span class="sxs-lookup"><span data-stu-id="32257-111">The XPS OM is essentially an in-memory version of an XPS document's contents.</span></span> <span data-ttu-id="32257-112">Bien qu’il soit similaire dans une organisation logique à un document XPS, un modèle d’objet XPS n’est pas considéré comme un document XPS tant qu’il n’a pas été sérialisé dans un fichier ou un flux.</span><span class="sxs-lookup"><span data-stu-id="32257-112">While similar in logical organization to an XPS document, an XPS OM is not considered an XPS document until it has been serialized to a file or a stream.</span></span>

<span data-ttu-id="32257-113">La structure exacte du balisage n’est pas disponible pour le modèle d’objet XPS lorsqu’un document XPS est désérialisé du balisage à un modèle d’objet XPS.</span><span class="sxs-lookup"><span data-stu-id="32257-113">The exact structure of the markup is not available to the XPS OM when an XPS document is deserialized from markup to an XPS OM.</span></span> <span data-ttu-id="32257-114">Par exemple, si la propriété a été représentée comme un élément ou un attribut dans le balisage, la valeur de la propriété d’un objet document est présentée par le modèle OM XPS exactement de la même façon.</span><span class="sxs-lookup"><span data-stu-id="32257-114">For example, whether the property was represented as an element or an attribute in the markup, the property value of a document object is presented by the XPS OM in exactly the same way.</span></span>

<span data-ttu-id="32257-115">L' [API de document XPS](documents-xps.md) peut être divisée selon les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="32257-115">The [XPS Document API](documents-xps.md) can be divided into the following categories:</span></span>

-   [<span data-ttu-id="32257-116">Interfaces du Trunk XPS OM</span><span class="sxs-lookup"><span data-stu-id="32257-116">XPS OM Trunk Interfaces</span></span>](xps-om-trunk-interfaces.md)

    <span data-ttu-id="32257-117">Les interfaces Trunk fournissent l’accès aux composants de niveau supérieur de la structure de document XPS.</span><span class="sxs-lookup"><span data-stu-id="32257-117">The trunk interfaces provide access to the top-level components of the XPS document structure.</span></span> <span data-ttu-id="32257-118">Ces interfaces fournissent également les moyens de sérialiser un modèle d’objet XPS et de désérialiser un document XPS.</span><span class="sxs-lookup"><span data-stu-id="32257-118">These interfaces also provide the means to serialize an XPS OM and deserialize an XPS document.</span></span>

-   [<span data-ttu-id="32257-119">Interfaces de page OM XPS</span><span class="sxs-lookup"><span data-stu-id="32257-119">XPS OM Page Interfaces</span></span>](xps-object-model-page-interfaces.md)

    <span data-ttu-id="32257-120">Les interfaces de page donnent accès au contenu d’une page dans un document XPS.</span><span class="sxs-lookup"><span data-stu-id="32257-120">The page interfaces provide access to the contents of a page in an XPS document.</span></span> <span data-ttu-id="32257-121">Les interfaces qui décrivent le contenu de la page sont également incluses avec les interfaces de page.</span><span class="sxs-lookup"><span data-stu-id="32257-121">The interfaces that describe the content of the page are also included with the page interfaces.</span></span>

-   [<span data-ttu-id="32257-122">Signatures numériques XPS OM</span><span class="sxs-lookup"><span data-stu-id="32257-122">XPS OM Digital Signatures</span></span>](using-the-xps-digital-signatures.md)

    <span data-ttu-id="32257-123">Le modèle d’objet XPS prend en charge les signatures numériques.</span><span class="sxs-lookup"><span data-stu-id="32257-123">The XPS OM supports digital signatures.</span></span> <span data-ttu-id="32257-124">Toutefois, vous pouvez accéder aux signatures numériques dans un document XPS directement sans créer un modèle d’objet XPS.</span><span class="sxs-lookup"><span data-stu-id="32257-124">However, you can access digital signatures in an XPS document directly without creating an XPS OM.</span></span> <span data-ttu-id="32257-125">Pour plus d’informations sur l’accès aux signatures numériques XPS sans modèle XPS, consultez [API de signature numérique XPS](xps-digital-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="32257-125">For more information about how to access XPS digital signatures without an XPS OM, see [XPS Digital Signature API](xps-digital-signatures.md).</span></span>

-   [<span data-ttu-id="32257-126">Interfaces du ticket d’impression XPS OM</span><span class="sxs-lookup"><span data-stu-id="32257-126">XPS OM Print Ticket Interfaces</span></span>](xps-object-model-print-ticket-interfaces.md)

    <span data-ttu-id="32257-127">Les documents XPS prennent en charge les tickets d’impression au niveau du package (travail), du document et de la page.</span><span class="sxs-lookup"><span data-stu-id="32257-127">XPS documents support print tickets at the package (job), document, and page level.</span></span> <span data-ttu-id="32257-128">Les tickets d’impression contiennent des informations sur la mise en forme du contenu du document pour l’impression ou l’affichage.</span><span class="sxs-lookup"><span data-stu-id="32257-128">Print tickets contain information about how to format document content for printing or viewing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32257-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="32257-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="32257-130">**Dans cette section**</span><span class="sxs-lookup"><span data-stu-id="32257-130">**In This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="32257-131">Interfaces du Trunk XPS OM</span><span class="sxs-lookup"><span data-stu-id="32257-131">XPS OM Trunk Interfaces</span></span>](xps-om-trunk-interfaces.md)
</dt> <dt>

[<span data-ttu-id="32257-132">Interfaces de page OM XPS</span><span class="sxs-lookup"><span data-stu-id="32257-132">XPS OM Page Interfaces</span></span>](xps-object-model-page-interfaces.md)
</dt> <dt>

[<span data-ttu-id="32257-133">Signatures numériques XPS OM</span><span class="sxs-lookup"><span data-stu-id="32257-133">XPS OM Digital Signatures</span></span>](using-the-xps-digital-signatures.md)
</dt> <dt>

[<span data-ttu-id="32257-134">Interfaces du ticket d’impression XPS OM</span><span class="sxs-lookup"><span data-stu-id="32257-134">XPS OM Print Ticket Interfaces</span></span>](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

<span data-ttu-id="32257-135">**Autres rubriques connexes**</span><span class="sxs-lookup"><span data-stu-id="32257-135">**Other Related Topics**</span></span>
</dt> <dt>

[<span data-ttu-id="32257-136">Initialiser un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="32257-136">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="32257-137">Signatures numériques XPS OM</span><span class="sxs-lookup"><span data-stu-id="32257-137">XPS OM Digital Signatures</span></span>](using-the-xps-digital-signatures.md)
</dt> <dt>

[<span data-ttu-id="32257-138">Informations de référence sur l’API de document XPS</span><span class="sxs-lookup"><span data-stu-id="32257-138">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="32257-139">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="32257-139">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



