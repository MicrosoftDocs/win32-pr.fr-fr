---
description: Flux de script ASF dans DirectShow
ms.assetid: afef1b8b-4be2-48a1-b72a-b2e6342a5e84
title: Flux de script ASF dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da279c654a581bdb9eba23371882c5cbefbf5849
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950265"
---
# <a name="asf-script-streams-in-directshow"></a><span data-ttu-id="66829-103">Flux de script ASF dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="66829-103">ASF Script Streams in DirectShow</span></span>

<span data-ttu-id="66829-104">Quand le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) reçoit un fichier qui comprend un flux de type WMMEDIATYPE \_ script, il crée une broche de sortie qui peut être connectée au filtre de [convertisseur de commande de script interne](internal-script-command-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="66829-104">When the [WM ASF Reader](wm-asf-reader-filter.md) filter is given a file that includes a stream of type WMMEDIATYPE\_Script, it creates an output pin for it that can be connected to the [Internal Script Command Renderer](internal-script-command-renderer-filter.md) filter.</span></span> <span data-ttu-id="66829-105">Quand vous appelez [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), ce filtre est automatiquement ajouté au graphique et connecté.</span><span class="sxs-lookup"><span data-stu-id="66829-105">When you call [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), that filter is automatically added to the graph and connected.</span></span> <span data-ttu-id="66829-106">Quand le convertisseur de commande de script interne reçoit un exemple contenant une commande de script, il déclenche un événement d' [**\_ \_ événement OLE EC**](ec-ole-event.md) dont *lParam* contient le script.</span><span class="sxs-lookup"><span data-stu-id="66829-106">When the Internal Script Command Renderer receives a sample containing a script command, it fires an [**EC\_OLE\_EVENT**](ec-ole-event.md) event whose *lParam* contains the script.</span></span> <span data-ttu-id="66829-107">L’application est entièrement responsable de la gestion de cet événement.</span><span class="sxs-lookup"><span data-stu-id="66829-107">The application is entirely responsible for handling this event.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66829-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="66829-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66829-109">Lecture de fichiers ASF dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="66829-109">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



