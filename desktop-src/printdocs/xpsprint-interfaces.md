---
description: .
ms.assetid: f575109e-e9c4-4db5-945c-7c96b6b5d613
title: Interfaces de l’API d’impression XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 828e999417354678d77ad1de8c29beb5956f7762
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755213"
---
# <a name="xps-print-api-interfaces"></a><span data-ttu-id="82bd7-103">Interfaces de l’API d’impression XPS</span><span class="sxs-lookup"><span data-stu-id="82bd7-103">XPS Print API Interfaces</span></span>

<span data-ttu-id="82bd7-104">\[Les interfaces décrites dans cette section sont déconseillées.</span><span class="sxs-lookup"><span data-stu-id="82bd7-104">\[The interfaces described in this section are deprecated.</span></span> <span data-ttu-id="82bd7-105">Les applications clientes doivent utiliser l' [API Print document package](./tailored-app-printing-api.md) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="82bd7-105">Client applications should use the [Print Document Package API](./tailored-app-printing-api.md) instead.\]</span></span>

<span data-ttu-id="82bd7-106">\[IXpsPrintJob n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="82bd7-106">\[IXpsPrintJob is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="82bd7-107">\]</span><span class="sxs-lookup"><span data-stu-id="82bd7-107">\]</span></span>

<span data-ttu-id="82bd7-108">\[IXpsPrintJobStream n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="82bd7-108">\[IXpsPrintJobStream is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="82bd7-109">\]</span><span class="sxs-lookup"><span data-stu-id="82bd7-109">\]</span></span>

## <a name="in-this-section"></a><span data-ttu-id="82bd7-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="82bd7-110">In this section</span></span>



| <span data-ttu-id="82bd7-111">Interface</span><span class="sxs-lookup"><span data-stu-id="82bd7-111">Interface</span></span>                                                   | <span data-ttu-id="82bd7-112">Description</span><span class="sxs-lookup"><span data-stu-id="82bd7-112">Description</span></span>                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82bd7-113">**IXpsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="82bd7-113">**IXpsPrintJob**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjob)<br/>             | <span data-ttu-id="82bd7-114">Permet d’accéder à un travail d’impression qui est actuellement en cours.</span><span class="sxs-lookup"><span data-stu-id="82bd7-114">Provides access to a print job that is currently in progress.</span></span><br/>                  |
| [<span data-ttu-id="82bd7-115">**IXpsPrintJobStream**</span><span class="sxs-lookup"><span data-stu-id="82bd7-115">**IXpsPrintJobStream**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjobstream)<br/> | <span data-ttu-id="82bd7-116">Interface de flux en écriture seule dans laquelle une application écrit des données de travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="82bd7-116">A write-only stream interface into which an application writes print job data.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="82bd7-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="82bd7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82bd7-118">Documents</span><span class="sxs-lookup"><span data-stu-id="82bd7-118">Documents</span></span>](./jobbindalldocuments.md)
</dt> <dt>

[<span data-ttu-id="82bd7-119">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="82bd7-119">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

