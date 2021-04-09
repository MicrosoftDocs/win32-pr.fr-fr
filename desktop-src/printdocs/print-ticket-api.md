---
description: L’API Print ticket fournit aux applications la possibilité de gérer et de convertir les tickets d’impression.
ms.assetid: 4f854c1a-f2e1-48c4-9cc1-8a0fcf1bebed
title: API ticket d’impression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e19cfd8d624a1390b8afacd625e92fcee2704dd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104042974"
---
# <a name="print-ticket-api"></a><span data-ttu-id="3c11c-103">API ticket d’impression</span><span class="sxs-lookup"><span data-stu-id="3c11c-103">Print Ticket API</span></span>

<span data-ttu-id="3c11c-104">L’API Print ticket fournit aux applications la possibilité de gérer et de convertir les tickets d’impression.</span><span class="sxs-lookup"><span data-stu-id="3c11c-104">The Print Ticket API provides enables applications to manage and convert print tickets.</span></span>

<span data-ttu-id="3c11c-105">Un ticket d’impression est un composant de document XPS qui contient les paramètres d’imprimante préférés pour une page dans un document ou pour un document entier, ou pour un travail d’impression qui contient un ou plusieurs documents.</span><span class="sxs-lookup"><span data-stu-id="3c11c-105">A print ticket is an XPS document component that contains the preferred printer settings for a page in a document, or for an entire document, or for a print job that contains one or more documents.</span></span> <span data-ttu-id="3c11c-106">Notez que les tickets d’impression sont uniquement disponibles dans les documents XPS.</span><span class="sxs-lookup"><span data-stu-id="3c11c-106">Note that print tickets are only found in XPS documents.</span></span>

<span data-ttu-id="3c11c-107">Pour que l’imprimante puisse utiliser le ticket d’impression, le ticket d’impression doit être validé par rapport aux caractéristiques de l’imprimante, qui sont définies dans les fonctionnalités d’impression de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="3c11c-107">Before the printer can use the print ticket, the print ticket must be validated against the printer's characteristics, which are defined in the printer's Print Capabilities.</span></span> <span data-ttu-id="3c11c-108">L’application effectue cette validation en appelant l’API Print ticket.</span><span class="sxs-lookup"><span data-stu-id="3c11c-108">The application performs that validation by calling the Print Ticket API.</span></span>

<span data-ttu-id="3c11c-109">PrintTicket et PrintCapabilities sont décrits à l’aide d’éléments du schéma d’impression, qui est défini par la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3c11c-109">The PrintTicket and PrintCapabilities are described by using elements of the Print Schema, which is defined by the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3c11c-110">Cette rubrique contient des informations sur les éléments d’API suivants :</span><span class="sxs-lookup"><span data-stu-id="3c11c-110">This topic contains information about the following API elements:</span></span>

-   [<span data-ttu-id="3c11c-111">Fonctions de l’API ticket d’impression</span><span class="sxs-lookup"><span data-stu-id="3c11c-111">Print Ticket API Functions</span></span>](print-ticket-api-functions.md)
-   [<span data-ttu-id="3c11c-112">Énumérations de l’API ticket d’impression</span><span class="sxs-lookup"><span data-stu-id="3c11c-112">Print Ticket API Enumerations</span></span>](print-ticket-api-enumerations.md)

<span data-ttu-id="3c11c-113">Le diagramme suivant montre la relation entre l’API ticket d’impression et les autres API d’impression qu’une application Windows Native peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="3c11c-113">The following diagram shows the relationship of the Print Ticket API to the other Print APIs that a native Windows application can use.</span></span>

![diagramme qui montre la relation entre l’API ticket d’impression et les autres API d’impression qu’une application Windows Native peut utiliser](images/print-apis-pt.png)

## <a name="related-topics"></a><span data-ttu-id="3c11c-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3c11c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c11c-116">API d’impression XPS</span><span class="sxs-lookup"><span data-stu-id="3c11c-116">XPS Print API</span></span>](xps-printing.md)
</dt> <dt>

[<span data-ttu-id="3c11c-117">API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="3c11c-117">Print Spooler API</span></span>](print-spooler-api.md)
</dt> <dt>

[<span data-ttu-id="3c11c-118">API d’impression GDI</span><span class="sxs-lookup"><span data-stu-id="3c11c-118">GDI Print API</span></span>](gdi-printing.md)
</dt> <dt>

[<span data-ttu-id="3c11c-119">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="3c11c-119">Print Schema Specification</span></span>](https://go.microsoft.com/fwlink/?linkid=2022117)
</dt> <dt>

[<span data-ttu-id="3c11c-120">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="3c11c-120">XML Paper Specification</span></span>](https://go.microsoft.com/fwlink/?linkid=2022122)
</dt> </dl>

 

 



