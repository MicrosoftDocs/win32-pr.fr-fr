---
title: Indépendance par rapport aux autres composants
description: Les données d’erreur étendues sont utiles même lorsque le serveur ou l’application par le biais duquel la chaîne transmise ne reconnaît pas les données d’erreur étendues ou ne les tire pas parti. Les approches recommandées pour ces situations sont fournies à la fin de cette section.
ms.assetid: 32c52afd-cd79-4df3-bf30-72a17ce22089
keywords:
- Indépendance par rapport aux autres composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba20a47a5bb30d8e23c1a90d666bc6b957ebb98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940253"
---
# <a name="independence-from-other-components"></a><span data-ttu-id="27b7d-105">Indépendance par rapport aux autres composants</span><span class="sxs-lookup"><span data-stu-id="27b7d-105">Independence From Other Components</span></span>

<span data-ttu-id="27b7d-106">Les données d’erreur étendues sont utiles même lorsque le serveur ou l’application par le biais duquel la chaîne transmise ne reconnaît pas les données d’erreur étendues ou ne les tire pas parti.</span><span class="sxs-lookup"><span data-stu-id="27b7d-106">Extended error data is useful even when the server or application through which the chain passed does not recognize extended error data, or does not take advantage of it.</span></span> <span data-ttu-id="27b7d-107">Les approches recommandées pour ces situations sont fournies à la fin de cette section.</span><span class="sxs-lookup"><span data-stu-id="27b7d-107">Recommended approaches for such situations are provided at the end of this section.</span></span>

<span data-ttu-id="27b7d-108">Les données d’erreur étendues sont particulièrement utiles lorsque les applications ou les serveurs qui utilisent RPC tirent parti des informations d’erreur étendues.</span><span class="sxs-lookup"><span data-stu-id="27b7d-108">Extended error data is most useful when applications or servers using RPC take advantage of extended error information.</span></span> <span data-ttu-id="27b7d-109">Lorsque vous examinez un \_ code d’erreur RPC S \_ \* et que les serveurs ou applications impliqués ne mettent pas à disposition des données d’erreur étendues, envisagez les approches suivantes :</span><span class="sxs-lookup"><span data-stu-id="27b7d-109">When investigating an RPC\_S\_\* error code and the servers or applications involved do not make extended error data available, consider the following approaches:</span></span>

-   <span data-ttu-id="27b7d-110">Jetez un espion.</span><span class="sxs-lookup"><span data-stu-id="27b7d-110">Take a sniff.</span></span>

    <span data-ttu-id="27b7d-111">Reproduisez le scénario tout en effectuant la détection.</span><span class="sxs-lookup"><span data-stu-id="27b7d-111">Reproduce the scenario while taking the sniff.</span></span> <span data-ttu-id="27b7d-112">La détection du câble contiendra les données d’erreur étendues.</span><span class="sxs-lookup"><span data-stu-id="27b7d-112">The sniff of the wire will contain the extended error data.</span></span>

-   <span data-ttu-id="27b7d-113">Examinez-le à partir du débogueur.</span><span class="sxs-lookup"><span data-stu-id="27b7d-113">Examine it from the debugger.</span></span>

    <span data-ttu-id="27b7d-114">Si la détection du problème ne fonctionne pas, car l’appel est local ou parce que l’erreur provient localement, attachez un débogueur au processus qui retourne l’erreur et placez un point d’arrêt immédiatement après l’appel RPC qui a généré l’erreur.</span><span class="sxs-lookup"><span data-stu-id="27b7d-114">If taking a sniff of the problem does not work, because the call is local or because the error originates locally, attach a debugger to the process returning the error and put a breakpoint immediately after the RPC call generating the error.</span></span> <span data-ttu-id="27b7d-115">Souvent, RPC indique des erreurs en levant des exceptions. par conséquent, si vous recherchez l’erreur 1825 (erreur s de l’appel RPC \_ s \_ \_ \_ ), activez l’exception 1825 et, lorsque le débogueur s’arrête sur cette exception, examinez les informations d’erreur étendues pour le thread.</span><span class="sxs-lookup"><span data-stu-id="27b7d-115">RPC often indicates errors by throwing exceptions, so if you are looking for error 1825 (RPC\_S\_SEC\_PKG\_ERROR), enable exception 1825 and when the debugger breaks on that exception, examine the extended error information for the thread.</span></span>

 

 




