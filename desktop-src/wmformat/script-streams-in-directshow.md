---
title: Flux de script dans DirectShow
description: Flux de script dans DirectShow
ms.assetid: ad467897-1d25-4bb0-a0ec-84560fe7063b
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, flux de scripts
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- ASF (Advanced Systems Format), flux de scripts
- ASF (format de systèmes avancés), flux de script
- DirectShow, flux de script
- flux de script, DirectShow
- flux, flux de script dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f08fab54dbdfe61dcc2ce78790cd471985cdeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311158"
---
# <a name="script-streams-in-directshow"></a><span data-ttu-id="6e203-112">Flux de script dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="6e203-112">Script Streams in DirectShow</span></span>

<span data-ttu-id="6e203-113">Quand le filtre de lecteur ASF WM reçoit un fichier qui comprend un flux de type WMMEDIATYPE \_ script, il crée une broche de sortie qui peut être connectée au filtre de convertisseur de commande de script interne DirectShow.</span><span class="sxs-lookup"><span data-stu-id="6e203-113">When the WM ASF Reader filter is given a file that includes a stream of type WMMEDIATYPE\_Script, it creates an output pin for it that can be connected to the DirectShow Internal Script Command Renderer filter.</span></span> <span data-ttu-id="6e203-114">Quand vous appelez **IGraphBuilder :: RenderFile**, ce filtre est automatiquement ajouté au graphique et connecté.</span><span class="sxs-lookup"><span data-stu-id="6e203-114">When you call **IGraphBuilder::RenderFile**, that filter is automatically added to the graph and connected.</span></span> <span data-ttu-id="6e203-115">Quand le convertisseur de commande de script interne reçoit un exemple contenant une commande de script, il déclenche un **\_ \_ événement OLE** de l’EC dont **lParam** contient le script.</span><span class="sxs-lookup"><span data-stu-id="6e203-115">When the Internal Script Command Renderer receives a sample containing a script command, it fires an **EC\_OLE\_EVENT** whose **lParam** contains the script.</span></span> <span data-ttu-id="6e203-116">L’application est entièrement responsable de la gestion de cet événement.</span><span class="sxs-lookup"><span data-stu-id="6e203-116">The application is entirely responsible for handling this event.</span></span> <span data-ttu-id="6e203-117">Pour plus d’informations sur l' **\_ \_ événement OLE EC**, consultez la documentation du kit de développement logiciel (SDK) DirectShow.</span><span class="sxs-lookup"><span data-stu-id="6e203-117">For more information on **EC\_OLE\_EVENT**, see the DirectShow SDK documentation.</span></span>

 

 




