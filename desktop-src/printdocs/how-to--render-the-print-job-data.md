---
description: Cette rubrique explique comment afficher les données du programme à imprimer.
ms.assetid: D1343C53-6F13-49FF-8C7C-25D5A3C31B22
title: 'Comment : afficher les données d’un travail d’impression'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2d9f8cbf68394fd56ebcf31cfb37ee8f337f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868533"
---
# <a name="how-to-render-print-job-data"></a><span data-ttu-id="d48db-103">Comment : afficher les données d’un travail d’impression</span><span class="sxs-lookup"><span data-stu-id="d48db-103">How To: Render Print Job Data</span></span>

<span data-ttu-id="d48db-104">Cette rubrique explique comment afficher les données du programme à imprimer.</span><span class="sxs-lookup"><span data-stu-id="d48db-104">This topic describes how to render the program data to be printed.</span></span> <span data-ttu-id="d48db-105">Cette rubrique n’explique pas en détail comment restituer des graphiques ou des images de texte spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d48db-105">This topic does not explain in detail about how to render specific graphics or text images.</span></span> <span data-ttu-id="d48db-106">Au lieu de cela, il décrit comment gérer les données du programme et les afficher sous la forme d’un document XPS, qu’il envoie à une imprimante à l’aide de l' [API d’impression XPS](xps-printing.md).</span><span class="sxs-lookup"><span data-stu-id="d48db-106">Instead, it describes how to manage the program data and render it as an XPS document, which it sends to a printer by using the [XPS Print API](xps-printing.md).</span></span>

## <a name="overview"></a><span data-ttu-id="d48db-107">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="d48db-107">Overview</span></span>

<span data-ttu-id="d48db-108">Le rendu des données de travail d’impression pour l’impression implique de placer les données spécifiques au programme, telles que le texte, les images et la mise en forme, et de les convertir dans un format compatible avec l’imprimante de destination.</span><span class="sxs-lookup"><span data-stu-id="d48db-108">Rendering print job data for printing involves taking the program-specific data, such as text, images, and formatting, and converting them into a format that is compatible with the destination printer.</span></span> <span data-ttu-id="d48db-109">Le programme qui envoie les données à l’imprimante doit l’envoyer dans le format requis par le pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="d48db-109">The program that sends the data to the printer must send it in the format that the printer driver requires.</span></span>

<span data-ttu-id="d48db-110">Utilisez l' [API d’impression XPS](xps-printing.md) pour envoyer les données à l’imprimante et les données doivent être formatées en tant que document XPS.</span><span class="sxs-lookup"><span data-stu-id="d48db-110">Use the [XPS Print API](xps-printing.md) to send the data to the printer and it requires the data to be formatted as an XPS document.</span></span> <span data-ttu-id="d48db-111">Pour produire le contenu du document XPS dont l’API d’impression XPS a besoin, l’exemple de programme utilise l' [API de document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d48db-111">To produce the XPS document content that the XPS Print API needs, the sample program uses the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span></span>

<span data-ttu-id="d48db-112">Si le contenu du programme est dans un format qui n’est pas compatible avec une imprimante, il doit être rendu avant d’être envoyé à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="d48db-112">If the program content is in a format that is not compatible with a printer, it will need to be rendered before it is sent to the printer.</span></span> <span data-ttu-id="d48db-113">Si le programme utilise l' [API de document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) pour gérer son contenu de programme, le contenu du programme sera dans un format qui peut être envoyé directement à l' [API d’impression XPS](xps-printing.md) et ne nécessitera pas de rendu supplémentaire avant de l’envoyer à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="d48db-113">If the program uses the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) to manage its program content, the program content will be in a format that can be sent directly to the [XPS Print API](xps-printing.md) and will not require any additional rendering before you send it to the printer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d48db-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d48db-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d48db-115">[API de document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d48db-115">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d48db-116">API d’impression XPS</span><span class="sxs-lookup"><span data-stu-id="d48db-116">XPS Print API</span></span>](xps-printing.md)
</dt> </dl>

 

 
