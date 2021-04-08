---
title: Bluetooth et getsockopt
description: Bluetooth utilise la fonction getsockopt pour interroger différents paramètres associés au canal du serveur ou à la connexion.
ms.assetid: 9593fd6c-b55d-45d8-a9d9-87ebcd09d1bd
keywords:
- Bluetooth
- getsockopt
- Bluetooth et getsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dede19b27eea39b7d1e778b3e92312a5e148c0ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728364"
---
# <a name="bluetooth-and-getsockopt"></a><span data-ttu-id="735a2-106">Bluetooth et getsockopt</span><span class="sxs-lookup"><span data-stu-id="735a2-106">Bluetooth and getsockopt</span></span>

<span data-ttu-id="735a2-107">Bluetooth utilise la fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) pour interroger différents paramètres associés au canal du serveur ou à la connexion.</span><span class="sxs-lookup"><span data-stu-id="735a2-107">Bluetooth uses the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function to query various parameters associated with the server channel or the connection.</span></span> <span data-ttu-id="735a2-108">L’utilisation de **getsockopt** avec Bluetooth présente les exigences suivantes :</span><span class="sxs-lookup"><span data-stu-id="735a2-108">Use of **getsockopt** with Bluetooth has the following requirements:</span></span>

-   <span data-ttu-id="735a2-109">Le paramètre *s* de [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) doit être un Socket Bluetooth valide.</span><span class="sxs-lookup"><span data-stu-id="735a2-109">The *s* parameter of [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) must be a valid Bluetooth socket.</span></span>
-   <span data-ttu-id="735a2-110">Le paramètre de *niveau* de [**GETSOCKOPT**](/windows/desktop/api/winsock/nf-winsock-getsockopt) doit être sol \_ RFCOMM.</span><span class="sxs-lookup"><span data-stu-id="735a2-110">The *level* parameter of [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) must be SOL\_RFCOMM.</span></span>

<span data-ttu-id="735a2-111">Pour obtenir la liste des options de Socket Bluetooth disponibles, consultez [options de socket et Bluetooth](bluetooth-and-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="735a2-111">For a listing of available Bluetooth socket options, see [Bluetooth and Socket Options](bluetooth-and-socket-options.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="735a2-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="735a2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="735a2-113">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="735a2-113">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="735a2-114">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="735a2-114">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> </dl>

 

 