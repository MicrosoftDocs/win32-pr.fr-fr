---
title: Débogage (services Web Windows)
description: Un ensemble de fonctions est uniquement disponible dans la version DEBUG et est conçu pour le test et le débogage.
ms.assetid: 23c01420-3f51-4c3f-9ee1-2614de3a278f
keywords:
- Débogage de services Web pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cad0abe916e068408cfda48184aa86e40029203
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106538804"
---
# <a name="debugging-windows-web-services"></a><span data-ttu-id="8c14b-106">Débogage (services Web Windows)</span><span class="sxs-lookup"><span data-stu-id="8c14b-106">Debugging (Windows Web Services)</span></span>

<span data-ttu-id="8c14b-107">Un ensemble de fonctions est uniquement disponible dans la version DEBUG et est conçu pour le test et le débogage.</span><span class="sxs-lookup"><span data-stu-id="8c14b-107">A set of functions is only available in the DEBUG build, and are intended for testing and debugging.</span></span>


<span data-ttu-id="8c14b-108">Un certain nombre de fonctions et de variables d’environnement sont disponibles uniquement en mode débogage.</span><span class="sxs-lookup"><span data-stu-id="8c14b-108">There are a number of functions and environment variables available in the DEBUG mode only.</span></span> <span data-ttu-id="8c14b-109">Ils peuvent être utilisés pour faciliter le test et le débogage.</span><span class="sxs-lookup"><span data-stu-id="8c14b-109">They can be used to help with testing and debugging.</span></span>

-   <span data-ttu-id="8c14b-110">La définition de WsTimeout = 0 entraîne l’infiniisation de tous les délais d’attente.</span><span class="sxs-lookup"><span data-stu-id="8c14b-110">Setting WsTimeout=0 will cause all timeouts to be INFINITE.</span></span> <span data-ttu-id="8c14b-111">Cela est utile lorsque vous exécutez pas à pas le débogueur pendant des opérations sensibles au temps.</span><span class="sxs-lookup"><span data-stu-id="8c14b-111">This is useful when stepping through the debugger during time sensitive operations.</span></span>
-   <span data-ttu-id="8c14b-112">La définition de WsFailCount a le même effet que l’appel de WsSetAutoFail.</span><span class="sxs-lookup"><span data-stu-id="8c14b-112">Setting WsFailCount has the same effect as calling WsSetAutoFail.</span></span>
-   <span data-ttu-id="8c14b-113">WsFlags vous permet de définir différents indicateurs qui modifient le comportement d’exécution.</span><span class="sxs-lookup"><span data-stu-id="8c14b-113">WsFlags allows you to set various flags that modify the runtime behavior.</span></span> <span data-ttu-id="8c14b-114">La syntaxe est WsFlags = a, b, c.</span><span class="sxs-lookup"><span data-stu-id="8c14b-114">The syntax is WsFlags=a,b,c.</span></span> <span data-ttu-id="8c14b-115">Les indicateurs pris en charge sont ModifyTimestamp, ModifyInclusivePrefixes, ModifyTimestampDigest, ModifyToHeaderDigest et ModifySignatureValue.</span><span class="sxs-lookup"><span data-stu-id="8c14b-115">The supported flags are ModifyTimestamp, ModifyInclusivePrefixes, ModifyTimestampDigest, ModifyToHeaderDigest and ModifySignatureValue.</span></span>

<span data-ttu-id="8c14b-116">Les fonctions suivantes sont utilisées avec le débogage :</span><span class="sxs-lookup"><span data-stu-id="8c14b-116">The following functions are used with debugging:</span></span>

-   [<span data-ttu-id="8c14b-117">**WsDumpMemory**</span><span class="sxs-lookup"><span data-stu-id="8c14b-117">**WsDumpMemory**</span></span>](wsdumpmemory.md)
-   [<span data-ttu-id="8c14b-118">**WsSetAutoFail**</span><span class="sxs-lookup"><span data-stu-id="8c14b-118">**WsSetAutoFail**</span></span>](wssetautofail.md)

 

 




