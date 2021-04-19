---
description: Fournit une interface au spouleur d’impression. Les applications peuvent utiliser cette API pour envoyer des documents XPS à une imprimante.
ms.assetid: df06ddcb-e573-461c-99a3-8f108fe2c143
title: API d’impression XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30c53322a8ae6a03c3ac4bb71fc680f719999546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518406"
---
# <a name="xps-print-api"></a><span data-ttu-id="cb441-104">API d’impression XPS</span><span class="sxs-lookup"><span data-stu-id="cb441-104">XPS Print API</span></span>

<span data-ttu-id="cb441-105">\[L’API d’impression XPS n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="cb441-105">\[The XPS Print API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="cb441-106">Les applications clientes doivent utiliser l' [API Print document package](./tailored-app-printing-api.md) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="cb441-106">Client applications should use the [Print Document Package API](./tailored-app-printing-api.md) instead.\]</span></span>

<span data-ttu-id="cb441-107">Fournit une interface au spouleur d’impression.</span><span class="sxs-lookup"><span data-stu-id="cb441-107">Provides an interface to the print spooler.</span></span> <span data-ttu-id="cb441-108">Les applications peuvent utiliser cette API pour envoyer des documents XPS à une imprimante.</span><span class="sxs-lookup"><span data-stu-id="cb441-108">Applications can use this API to send XPS documents to a printer.</span></span>

<span data-ttu-id="cb441-109">Cette section contient des informations sur les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="cb441-109">This section contains information about the following topics.</span></span>

<dl>

[<span data-ttu-id="cb441-110">À propos de l’API d’impression XPS</span><span class="sxs-lookup"><span data-stu-id="cb441-110">About the XPS Print API</span></span>](about-xps-print-api.md)  
[<span data-ttu-id="cb441-111">Utilisation de l’API d’impression XPS</span><span class="sxs-lookup"><span data-stu-id="cb441-111">Using the XPS Print API</span></span>](using-the-xps-print-api.md)  
[<span data-ttu-id="cb441-112">Informations de référence sur l’API d’impression XPS</span><span class="sxs-lookup"><span data-stu-id="cb441-112">XPS Print API Reference</span></span>](xpsprint-interfaces.md)  
</dl>

<span data-ttu-id="cb441-113">Les applications Windows natives qui créent des documents XPS, par exemple à l’aide de l' [API de document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)), peuvent utiliser l’API d’impression XPS pour envoyer du contenu de document XPS à une imprimante.</span><span class="sxs-lookup"><span data-stu-id="cb441-113">Native Windows applications that create XPS documents, such as by using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)), can use the XPS Print API to send XPS document content to a printer.</span></span>

<span data-ttu-id="cb441-114">Le diagramme suivant montre la relation entre l’API d’impression XPS et les autres API d’impression qu’une application Windows Native peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="cb441-114">The following diagram shows the relationship of the XPS Print API to the other Print APIs that a native Windows application can use.</span></span>

![diagramme qui montre la relation entre l’API d’impression XPS et les autres API d’impression qu’une application Windows Native peut utiliser](images/print-apis-xps.png)

## <a name="related-topics"></a><span data-ttu-id="cb441-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cb441-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb441-117">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="cb441-117">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="cb441-118">API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="cb441-118">Print Spooler API</span></span>](print-spooler-api.md)
</dt> <dt>

[<span data-ttu-id="cb441-119">API ticket d’impression</span><span class="sxs-lookup"><span data-stu-id="cb441-119">Print Ticket API</span></span>](print-ticket-api.md)
</dt> <dt>

[<span data-ttu-id="cb441-120">API d’impression GDI</span><span class="sxs-lookup"><span data-stu-id="cb441-120">GDI Print API</span></span>](gdi-printing.md)
</dt> </dl>

 

 
