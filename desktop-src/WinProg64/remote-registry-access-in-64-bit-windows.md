---
title: Accès au Registre distant dans Windows 64 bits
description: Le redirecteur du Registre fournit un accès à distance au registre sur Windows 64 bits via la fonction RegConnectRegistry.
ms.assetid: 7873c1e2-53fb-4c93-bf4c-251a13cd8db7
keywords:
- accès au registre à distance, programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a139198ca08e0fdb9d7bcb070dcabf89dfa5403
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106540764"
---
# <a name="remote-registry-access-in-64-bit-windows"></a><span data-ttu-id="434a4-104">Accès au Registre distant dans Windows 64 bits</span><span class="sxs-lookup"><span data-stu-id="434a4-104">Remote Registry Access in 64-bit Windows</span></span>

<span data-ttu-id="434a4-105">Le redirecteur du Registre fournit un accès à distance au registre sur Windows 64 bits via la fonction [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) .</span><span class="sxs-lookup"><span data-stu-id="434a4-105">The registry redirector provides remote access to the registry on 64-bit Windows through the [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) function.</span></span>

<span data-ttu-id="434a4-106">Si le client est une application 32 bits, il accède à la vue de Registre 32 bits par défaut du serveur.</span><span class="sxs-lookup"><span data-stu-id="434a4-106">If the client is a 32-bit application, it accesses the server's default 32-bit registry view.</span></span> <span data-ttu-id="434a4-107">Si le client est une application 64 bits, il accède à la vue de Registre 64 bits.</span><span class="sxs-lookup"><span data-stu-id="434a4-107">If the client is a 64-bit application, it accesses the 64-bit registry view.</span></span>

<span data-ttu-id="434a4-108">**Windows Server 2003 :** Tous les clients accèdent à la vue de Registre 64 bits, sauf si l’application utilise l’indicateur de clé \_ WOW64 \_ 32KEY.</span><span class="sxs-lookup"><span data-stu-id="434a4-108">**Windows Server 2003:** All clients access the 64-bit registry view unless the application uses the KEY\_WOW64\_32KEY flag.</span></span> <span data-ttu-id="434a4-109">Ce comportement a changé avec Windows Server 2003 avec Service Pack 1 (SP1) et Windows XP Professionnel Édition x64, à condition que le client et le serveur exécutent ces versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="434a4-109">This behavior changed with Windows Server 2003 with Service Pack 1 (SP1) and Windows XP Professional x64 Edition, provided that both the client and the server are running these versions of Windows.</span></span>

## <a name="related-topics"></a><span data-ttu-id="434a4-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="434a4-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="434a4-111">Redirecteur du Registre</span><span class="sxs-lookup"><span data-stu-id="434a4-111">Registry Redirector</span></span>](registry-redirector.md)
</dt> <dt>

[<span data-ttu-id="434a4-112">Réflexion du Registre</span><span class="sxs-lookup"><span data-stu-id="434a4-112">Registry Reflection</span></span>](registry-reflection.md)
</dt> </dl>

 

 