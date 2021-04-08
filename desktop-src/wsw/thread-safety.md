---
title: Cohérence de thread
description: Toutes les fonctions de cette API peuvent être appelées en toute sécurité à partir de différents threads. Toutefois, chaque objet passé en tant que paramètre aux fonctions a un comportement de thread spécifique, comme décrit ci-dessous.
ms.assetid: 712d6750-884e-421a-8ecf-efcd4ec9b21d
keywords:
- Services Web de sécurité des threads pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed84cac9634148742c92f1b0d4b4ecdb905ac42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734852"
---
# <a name="thread-safety"></a><span data-ttu-id="ef2c4-107">Cohérence de thread</span><span class="sxs-lookup"><span data-stu-id="ef2c4-107">Thread Safety</span></span>

<span data-ttu-id="ef2c4-108">Toutes les fonctions de cette API peuvent être appelées en toute sécurité à partir de différents threads.</span><span class="sxs-lookup"><span data-stu-id="ef2c4-108">All functions in this API are safe to call concurrently from different threads.</span></span> <span data-ttu-id="ef2c4-109">Toutefois, chaque objet passé en tant que paramètre aux fonctions a un comportement de thread spécifique, comme décrit ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="ef2c4-109">However, each object passed as a parameter to the functions have specific threading behavior, as described below.</span></span>


<span data-ttu-id="ef2c4-110">Les descripteurs suivants sont à thread unique et ne prennent pas en charge les opérations simultanées pour une instance particulière :</span><span class="sxs-lookup"><span data-stu-id="ef2c4-110">The following handles are single threaded and do not support concurrent operations for a particular instance:</span></span>

-   [<span data-ttu-id="ef2c4-111">\_tas WS</span><span class="sxs-lookup"><span data-stu-id="ef2c4-111">WS\_HEAP</span></span>](ws-heap.md)
-   [<span data-ttu-id="ef2c4-112">\_message WS</span><span class="sxs-lookup"><span data-stu-id="ef2c4-112">WS\_MESSAGE</span></span>](ws-message.md)
-   [<span data-ttu-id="ef2c4-113">\_ \_ mémoire tampon XML WS</span><span class="sxs-lookup"><span data-stu-id="ef2c4-113">WS\_XML\_BUFFER</span></span>](ws-xml-buffer.md)
-   [<span data-ttu-id="ef2c4-114">\_lecteur XML \_ WS</span><span class="sxs-lookup"><span data-stu-id="ef2c4-114">WS\_XML\_READER</span></span>](ws-xml-reader.md)
-   [<span data-ttu-id="ef2c4-115">\_enregistreur XML \_ WS</span><span class="sxs-lookup"><span data-stu-id="ef2c4-115">WS\_XML\_WRITER</span></span>](ws-xml-writer.md)
-   [<span data-ttu-id="ef2c4-116">\_erreur WS</span><span class="sxs-lookup"><span data-stu-id="ef2c4-116">WS\_ERROR</span></span>](ws-error.md)
-   [<span data-ttu-id="ef2c4-117">contexte de l' \_ opération WS \_</span><span class="sxs-lookup"><span data-stu-id="ef2c4-117">WS\_OPERATION\_CONTEXT</span></span>](ws-operation-context.md)
-   [<span data-ttu-id="ef2c4-118">\_stratégie WS</span><span class="sxs-lookup"><span data-stu-id="ef2c4-118">WS\_POLICY</span></span>](ws-policy.md)
-   [<span data-ttu-id="ef2c4-119">\_métadonnées WS</span><span class="sxs-lookup"><span data-stu-id="ef2c4-119">WS\_METADATA</span></span>](ws-metadata.md)
-   [<span data-ttu-id="ef2c4-120">\_jeton de sécurité WS \_</span><span class="sxs-lookup"><span data-stu-id="ef2c4-120">WS\_SECURITY\_TOKEN</span></span>](ws-security-token.md)
-   [<span data-ttu-id="ef2c4-121">\_contexte de sécurité WS \_</span><span class="sxs-lookup"><span data-stu-id="ef2c4-121">WS\_SECURITY\_CONTEXT</span></span>](ws-security-context.md)

<span data-ttu-id="ef2c4-122">Les handles suivants sont des threads libres et prennent en charge les opérations simultanées pour une instance particulière :</span><span class="sxs-lookup"><span data-stu-id="ef2c4-122">The following handles are free threaded and do support concurrent operations for a particular instance:</span></span>

-   [<span data-ttu-id="ef2c4-123">\_canal WS</span><span class="sxs-lookup"><span data-stu-id="ef2c4-123">WS\_CHANNEL</span></span>](ws-channel.md)
-   [<span data-ttu-id="ef2c4-124">\_écouteur WS</span><span class="sxs-lookup"><span data-stu-id="ef2c4-124">WS\_LISTENER</span></span>](ws-listener.md)
-   [<span data-ttu-id="ef2c4-125">\_hôte de service WS \_</span><span class="sxs-lookup"><span data-stu-id="ef2c4-125">WS\_SERVICE\_HOST</span></span>](ws-service-host.md)
-   [<span data-ttu-id="ef2c4-126">\_proxy WS service \_</span><span class="sxs-lookup"><span data-stu-id="ef2c4-126">WS\_SERVICE\_PROXY</span></span>](ws-service-proxy.md)

<span data-ttu-id="ef2c4-127">Pour tous ces handles, le Threading est défini en termes d’opérations (pas d’appels de fonction).</span><span class="sxs-lookup"><span data-stu-id="ef2c4-127">For all these handles, threading is defined in terms of operations (not function calls).</span></span> <span data-ttu-id="ef2c4-128">Une opération est définie différemment pour les fonctions appelées de façon synchrone par rapport aux fonctions appelées de façon asynchrone :</span><span class="sxs-lookup"><span data-stu-id="ef2c4-128">An operation is defined differently for functions invoked synchronously versus functions invoked asynchronously:</span></span>

-   <span data-ttu-id="ef2c4-129">Pour les fonctions appelées de façon synchrone, l’opération est en attente pendant l’exécution de la fonction.</span><span class="sxs-lookup"><span data-stu-id="ef2c4-129">For functions invoked synchronously, the operation is pending during the execution of the function.</span></span>
-   <span data-ttu-id="ef2c4-130">Pour les fonctions appelées de façon asynchrone, si la fonction retourne un code de retour autre que **WS \_ S \_ Async** , l’opération est en attente pendant l’exécution de la fonction.</span><span class="sxs-lookup"><span data-stu-id="ef2c4-130">For functions invoked asynchronously, if the function returns a return code other than **WS\_S\_ASYNC** the operation is pending during the execution of the function.</span></span> <span data-ttu-id="ef2c4-131">Toutefois, si la fonction retourne **WS \_ S \_ Async** , l’opération est en attente jusqu’à ce que le [**\_ \_ rappel WS Async**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) soit appelé.</span><span class="sxs-lookup"><span data-stu-id="ef2c4-131">If the function returns **WS\_S\_ASYNC** , however, the operation is pending until the [**WS\_ASYNC\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) is invoked.</span></span> <span data-ttu-id="ef2c4-132">Pour plus d’informations sur l’appel de fonctions de manière asynchrone, consultez la rubrique [modèle asynchrone](asynchronous-model.md) .</span><span class="sxs-lookup"><span data-stu-id="ef2c4-132">For more information about invoking functions asynchronously, see the [Asynchronous Model](asynchronous-model.md) topic.</span></span> <span data-ttu-id="ef2c4-133">Pour les codes d’erreur, consultez [valeurs de retour des services Web Windows](windows-web-services-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ef2c4-133">For error codes, see [Windows Web Services Return Values](windows-web-services-return-values.md).</span></span>

<span data-ttu-id="ef2c4-134">Le fait de ne pas suivre le contrat de thread d’un objet entraîne un comportement indéfini.</span><span class="sxs-lookup"><span data-stu-id="ef2c4-134">Failure to follow the threading contract for an object will result in undefined behavior.</span></span>

 

 




