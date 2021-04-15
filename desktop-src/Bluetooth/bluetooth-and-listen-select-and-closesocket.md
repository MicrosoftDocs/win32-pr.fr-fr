---
title: Bluetooth et écouter, sélectionner et opération closesocket
description: Bluetooth utilise les fonctions Listen, SELECT et opération closesocket sans aucune modification de la programmation Windows Sockets standard.
ms.assetid: b64440de-bc63-4e3b-bfd9-5cf783f36c23
keywords:
- Bluetooth
- opération closesocket
- listen
- select
- Bluetooth et écouter
- Bluetooth et écouter, sélectionner
- Bluetooth et écouter, sélectionner et opération closesocket
- listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e442cfc0593ab5be297902487c7c3ccdf056b4e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463338"
---
# <a name="bluetooth-and-listen-select-and-closesocket"></a><span data-ttu-id="d3b7e-111">Bluetooth et écouter, sélectionner et opération closesocket</span><span class="sxs-lookup"><span data-stu-id="d3b7e-111">Bluetooth and listen, select, and closesocket</span></span>

<span data-ttu-id="d3b7e-112">Bluetooth utilise les fonctions [**Listen**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**Select**](/windows/desktop/api/winsock2/nf-winsock2-select)et [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) sans aucune modification de la programmation Windows Sockets standard.</span><span class="sxs-lookup"><span data-stu-id="d3b7e-112">Bluetooth uses the [**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**select**](/windows/desktop/api/winsock2/nf-winsock2-select), and [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) functions without any modification from standard Windows Sockets programming.</span></span>

<span data-ttu-id="d3b7e-113">Comme avec Windows Sockets, la fonction [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) libère les ressources associées au socket.</span><span class="sxs-lookup"><span data-stu-id="d3b7e-113">As with Windows Sockets, the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function frees resources associated with the socket.</span></span>

<span data-ttu-id="d3b7e-114">Lors de l’appel de la fonction [**Listen**](/windows/desktop/api/winsock2/nf-winsock2-listen) , il est fortement recommandé d’utiliser une valeur basse pour le paramètre *backlog* (généralement 2 à 4), car seules quelques connexions client sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="d3b7e-114">When calling the [**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen) function, it is strongly recommended that a low value is used for the *backlog* parameter (typically 2 to 4), since only a few client connections are accepted.</span></span> <span data-ttu-id="d3b7e-115">Cela réduit les ressources système allouées pour une utilisation par le socket d’écoute.</span><span class="sxs-lookup"><span data-stu-id="d3b7e-115">This reduces the system resources that are allocated for use by the listening socket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3b7e-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3b7e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3b7e-117">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="d3b7e-117">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="d3b7e-118">**opération closesocket**</span><span class="sxs-lookup"><span data-stu-id="d3b7e-118">**closesocket**</span></span>](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[<span data-ttu-id="d3b7e-119">**Journal**</span><span class="sxs-lookup"><span data-stu-id="d3b7e-119">**listen**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-listen)
</dt> <dt>

[<span data-ttu-id="d3b7e-120">**sélectionné**</span><span class="sxs-lookup"><span data-stu-id="d3b7e-120">**select**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-select)
</dt> </dl>

 

 