---
title: Commandes netsh pour HTTP
description: Vous pouvez utiliser les commandes netsh pour le contexte HTTP pour interroger et configurer HTTP.sys paramètres et paramètres.
ms.assetid: 695c309c-ab43-4c6a-b5f6-5bb9f715bf71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55f6e0fdd0813284e36d2fb9fb826929c67df63c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674557"
---
# <a name="netsh-commands-for-http"></a><span data-ttu-id="00116-103">Commandes netsh pour HTTP</span><span class="sxs-lookup"><span data-stu-id="00116-103">Netsh commands for HTTP</span></span>

<span data-ttu-id="00116-104">Vous pouvez utiliser les commandes netsh pour le contexte HTTP pour interroger et configurer HTTP.sys paramètres et paramètres.</span><span class="sxs-lookup"><span data-stu-id="00116-104">You can use the Netsh commands for HTTP context to query and configure HTTP.sys settings and parameters.</span></span>

<span data-ttu-id="00116-105">Vous pouvez exécuter ces commandes à partir de l’invite de commandes dans le système d’exploitation Windows Vista ou à partir de l’invite de commandes pour le contexte **netsh http** .</span><span class="sxs-lookup"><span data-stu-id="00116-105">You can run these commands at the command prompt in the Windows Vista operating system or at the command prompt for the **netsh http** context.</span></span> <span data-ttu-id="00116-106">Pour que ces commandes fonctionnent à l’invite de commandes dans Windows Vista, vous devez taper **netsh http** avant de taper des commandes et des paramètres tels qu’ils apparaissent dans la syntaxe ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="00116-106">For these commands to work at the command prompt in Windows Vista, you must type **netsh http** before typing commands and parameters as they appear in the syntax below.</span></span> <span data-ttu-id="00116-107">Pour afficher l’aide d’une commande à l’invite de commandes, tapez \* CommandName \***/ ?**, où *CommandName* est le nom de la commande.</span><span class="sxs-lookup"><span data-stu-id="00116-107">To view help for a command at the command prompt, type \*CommandName\***/?**, where *CommandName* is the name of the command.</span></span>

<span data-ttu-id="00116-108">Pour afficher la syntaxe de la commande, consultez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="00116-108">To view the command syntax, see the commands:</span></span>

-   [<span data-ttu-id="00116-109">**add iplisten**</span><span class="sxs-lookup"><span data-stu-id="00116-109">**add iplisten**</span></span>](add-iplisten.md)
-   [<span data-ttu-id="00116-110">**add sslcert**</span><span class="sxs-lookup"><span data-stu-id="00116-110">**add sslcert**</span></span>](add-sslcert.md)
-   [<span data-ttu-id="00116-111">**add timeout**</span><span class="sxs-lookup"><span data-stu-id="00116-111">**add timeout**</span></span>](add-timeout.md)
-   [<span data-ttu-id="00116-112">**add urlacl**</span><span class="sxs-lookup"><span data-stu-id="00116-112">**add urlacl**</span></span>](add-urlacl.md)
-   [<span data-ttu-id="00116-113">**supprimer le cache**</span><span class="sxs-lookup"><span data-stu-id="00116-113">**delete cache**</span></span>](delete-cache.md)
-   [<span data-ttu-id="00116-114">**delete iplisten**</span><span class="sxs-lookup"><span data-stu-id="00116-114">**delete iplisten**</span></span>](delete-iplisten.md)
-   [<span data-ttu-id="00116-115">**delete sslcert**</span><span class="sxs-lookup"><span data-stu-id="00116-115">**delete sslcert**</span></span>](delete-sslcert.md)
-   [<span data-ttu-id="00116-116">**delete timeout**</span><span class="sxs-lookup"><span data-stu-id="00116-116">**delete timeout**</span></span>](delete-timeout.md)
-   [<span data-ttu-id="00116-117">**delete urlacl**</span><span class="sxs-lookup"><span data-stu-id="00116-117">**delete urlacl**</span></span>](delete-urlacl.md)
-   [<span data-ttu-id="00116-118">**flush logbuffer**</span><span class="sxs-lookup"><span data-stu-id="00116-118">**flush logbuffer**</span></span>](flush-logbuffer.md)
-   [<span data-ttu-id="00116-119">**show cachestate**</span><span class="sxs-lookup"><span data-stu-id="00116-119">**show cachestate**</span></span>](show-cachestate.md)
-   [<span data-ttu-id="00116-120">**show iplisten**</span><span class="sxs-lookup"><span data-stu-id="00116-120">**show iplisten**</span></span>](show-iplisten.md)
-   [<span data-ttu-id="00116-121">**show servicestate**</span><span class="sxs-lookup"><span data-stu-id="00116-121">**show servicestate**</span></span>](show-servicestate.md)
-   [<span data-ttu-id="00116-122">**show sslcert**</span><span class="sxs-lookup"><span data-stu-id="00116-122">**show sslcert**</span></span>](show-sslcert.md)
-   [<span data-ttu-id="00116-123">**show timeout**</span><span class="sxs-lookup"><span data-stu-id="00116-123">**show timeout**</span></span>](show-timeout.md)
-   [<span data-ttu-id="00116-124">**show urlacl**</span><span class="sxs-lookup"><span data-stu-id="00116-124">**show urlacl**</span></span>](show-urlacl.md)

 

 




