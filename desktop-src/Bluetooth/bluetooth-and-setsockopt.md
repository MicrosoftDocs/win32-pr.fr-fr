---
title: Bluetooth et setsockopt
description: Bluetooth utilise la fonction Setsockopt pour définir différents paramètres associés au canal du serveur ou à la connexion.
ms.assetid: ab78baed-5556-4d7b-88a6-e3ceb93afa8c
keywords:
- Bluetooth
- setsockopt
- Bluetooth et setsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 943839a49788b76e597596aee9cba65fa4b8d30d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315342"
---
# <a name="bluetooth-and-setsockopt"></a><span data-ttu-id="6b4e4-106">Bluetooth et setsockopt</span><span class="sxs-lookup"><span data-stu-id="6b4e4-106">Bluetooth and setsockopt</span></span>

<span data-ttu-id="6b4e4-107">Bluetooth utilise la fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) pour définir différents paramètres associés au canal du serveur ou à la connexion.</span><span class="sxs-lookup"><span data-stu-id="6b4e4-107">Bluetooth uses the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to set various parameters associated with the server channel or the connection.</span></span> <span data-ttu-id="6b4e4-108">L’utilisation de **setsockopt** avec Bluetooth présente les exigences suivantes :</span><span class="sxs-lookup"><span data-stu-id="6b4e4-108">Use of **setsockopt** with Bluetooth has the following requirements:</span></span>

-   <span data-ttu-id="6b4e4-109">Le paramètre *s* de [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) doit être un Socket Bluetooth valide.</span><span class="sxs-lookup"><span data-stu-id="6b4e4-109">The *s* parameter of [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) must be a valid Bluetooth socket.</span></span>
-   <span data-ttu-id="6b4e4-110">Le paramètre de *niveau* de [**SETSOCKOPT**](/windows/desktop/api/winsock/nf-winsock-setsockopt) doit être sol \_ RFCOMM.</span><span class="sxs-lookup"><span data-stu-id="6b4e4-110">The *level* parameter of [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) must be SOL\_RFCOMM.</span></span>

<span data-ttu-id="6b4e4-111">Pour obtenir la liste des options de Socket Bluetooth disponibles, consultez [options de socket et Bluetooth](bluetooth-and-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="6b4e4-111">For a listing of available Bluetooth socket options, see [Bluetooth and Socket Options](bluetooth-and-socket-options.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b4e4-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6b4e4-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b4e4-113">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="6b4e4-113">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="6b4e4-114">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="6b4e4-114">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 