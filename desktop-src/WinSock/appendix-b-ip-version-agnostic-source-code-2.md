---
description: Cette annexe illustre une version réécrite des exemples d’applications Simplec. c et simple. c qui gère correctement le code du serveur CodeIPv6-Enabled du client IPv4 ou IPv6.
ms.assetid: ffcbd59e-63ea-4df3-9db9-e7d4634eefeb
title: 'Annexe B : code source agnostique de la version IP'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333e344376695122ebcd650ebf2595d70afbf7ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862593"
---
# <a name="appendix-b-ip-version-agnostic-source-code"></a><span data-ttu-id="df1b4-103">Annexe B : code source agnostique de la version IP</span><span class="sxs-lookup"><span data-stu-id="df1b4-103">Appendix B: IP-version Agnostic Source Code</span></span>

<span data-ttu-id="df1b4-104">Cette annexe illustre une version réécrite des exemples d’applications Simplec. c et simple. c qui gère en douceur IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="df1b4-104">This appendix illustrates a rewritten version of the Simplec.c and Simples.c sample applications that gracefully handles either IPv4 or IPv6.</span></span>

-   [<span data-ttu-id="df1b4-105">Code client compatible IPv6</span><span class="sxs-lookup"><span data-stu-id="df1b4-105">IPv6-Enabled Client Code</span></span>](ipv6-enabled-client-code-2.md)
-   [<span data-ttu-id="df1b4-106">Code serveur compatible IPv6</span><span class="sxs-lookup"><span data-stu-id="df1b4-106">IPv6-Enabled Server Code</span></span>](ipv6-enabled-server-code-2.md)

<span data-ttu-id="df1b4-107">Ce code illustre les instructions énoncées dans ce guide IPv6 et est inclus pour fournir le code source qui a été correctement modifié pour ajouter la prise en charge d’IPv6.</span><span class="sxs-lookup"><span data-stu-id="df1b4-107">This code exemplifies the guidelines set forth in this IPv6 guide, and is included to provide source code that has been successfully modified to add support for IPv6.</span></span> <span data-ttu-id="df1b4-108">Cet exemple est volontairement simple, mais il fournit un exemple pratique pour l’utilisation et la révision de.</span><span class="sxs-lookup"><span data-stu-id="df1b4-108">This sample is intentionally simple, but provides a hands-on sample for perusing and reviewing.</span></span> <span data-ttu-id="df1b4-109">Une version IPv4 uniquement de ce code source est fournie dans [annexe A : code source IPv4 uniquement](appendix-a-ipv4-only-source-code-2.md).</span><span class="sxs-lookup"><span data-stu-id="df1b4-109">An IPv4 only version of this source code is provided in [Appendix A: IPv4-only Source Code](appendix-a-ipv4-only-source-code-2.md).</span></span>

<span data-ttu-id="df1b4-110">En comparant le code source de l’annexe A (IPv4 uniquement) et l’annexe B (IP-version agnostique), vous avez une idée des modifications nécessaires à la modification de votre application Windows Sockets afin d’ajouter la prise en charge d’IPv6.</span><span class="sxs-lookup"><span data-stu-id="df1b4-110">By comparing the source code in Appendix A (IPv4 only) and Appendix B (IP-version agnostic), you get a sense of the changes necessary to modify your Windows Sockets application to add support for IPv6.</span></span>

 

 



