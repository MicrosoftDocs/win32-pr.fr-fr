---
description: Interfaces de l’API d’impression XPS
ms.assetid: f575109e-e9c4-4db5-945c-7c96b6b5d613
title: Interfaces de l’API d’impression XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47cd01c169c82a9e3210f281ec6c44fa206c40b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105187"
---
# <a name="xps-print-api-interfaces"></a><span data-ttu-id="75a0c-103">Interfaces de l’API d’impression XPS</span><span class="sxs-lookup"><span data-stu-id="75a0c-103">XPS Print API Interfaces</span></span>

<span data-ttu-id="75a0c-104">\[Les interfaces décrites dans cette section sont déconseillées.</span><span class="sxs-lookup"><span data-stu-id="75a0c-104">\[The interfaces described in this section are deprecated.</span></span> <span data-ttu-id="75a0c-105">Les applications clientes doivent utiliser l' [API Print document package](./tailored-app-printing-api.md) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="75a0c-105">Client applications should use the [Print Document Package API](./tailored-app-printing-api.md) instead.\]</span></span>

<span data-ttu-id="75a0c-106">\[IXpsPrintJob n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="75a0c-106">\[IXpsPrintJob is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="75a0c-107">\]</span><span class="sxs-lookup"><span data-stu-id="75a0c-107">\]</span></span>

<span data-ttu-id="75a0c-108">\[IXpsPrintJobStream n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="75a0c-108">\[IXpsPrintJobStream is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="75a0c-109">\]</span><span class="sxs-lookup"><span data-stu-id="75a0c-109">\]</span></span>

## <a name="in-this-section"></a><span data-ttu-id="75a0c-110">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="75a0c-110">In this section</span></span>



| <span data-ttu-id="75a0c-111">Interface</span><span class="sxs-lookup"><span data-stu-id="75a0c-111">Interface</span></span>                                                   | <span data-ttu-id="75a0c-112">Description</span><span class="sxs-lookup"><span data-stu-id="75a0c-112">Description</span></span>                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75a0c-113">**IXpsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="75a0c-113">**IXpsPrintJob**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjob)<br/>             | <span data-ttu-id="75a0c-114">Permet d’accéder à un travail d’impression qui est actuellement en cours.</span><span class="sxs-lookup"><span data-stu-id="75a0c-114">Provides access to a print job that is currently in progress.</span></span><br/>                  |
| [<span data-ttu-id="75a0c-115">**IXpsPrintJobStream**</span><span class="sxs-lookup"><span data-stu-id="75a0c-115">**IXpsPrintJobStream**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjobstream)<br/> | <span data-ttu-id="75a0c-116">Interface de flux en écriture seule dans laquelle une application écrit des données de travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="75a0c-116">A write-only stream interface into which an application writes print job data.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="75a0c-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="75a0c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75a0c-118">Documents</span><span class="sxs-lookup"><span data-stu-id="75a0c-118">Documents</span></span>](./jobbindalldocuments.md)
</dt> <dt>

[<span data-ttu-id="75a0c-119">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="75a0c-119">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

