---
title: Développement d’un serveur RPC à hautes performances
description: Les informations contenues dans cette section s’appliquent aux séquences de protocoles distants ncacn \_ IP \_ TCP, ncacn \_ http, ncacn \_ np et à Windows 2000 et Windows XP.
ms.assetid: 7b4239af-951b-4d1b-8ac3-224279f6929e
keywords:
- Appel de procédure distante RPC, meilleures pratiques, développement d’un serveur hautes performances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a18319c1f4ade80ae026b68c8f5540030b992b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463582"
---
# <a name="developing-a-high-performance-rpc-server"></a><span data-ttu-id="01ec2-104">Développement d’un serveur RPC à hautes performances</span><span class="sxs-lookup"><span data-stu-id="01ec2-104">Developing a High Performance RPC Server</span></span>

<span data-ttu-id="01ec2-105">Les informations contenues dans cette section s’appliquent aux séquences de protocoles distants : [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp), [**ncacn \_ http**](/windows/desktop/Midl/ncacn-http), [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np)et Windows 2000 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="01ec2-105">The information in this section applies to remote protocol sequences: [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp), [**ncacn\_http**](/windows/desktop/Midl/ncacn-http), [**ncacn\_np**](/windows/desktop/Midl/ncacn-np), and to Windows 2000 and Windows XP.</span></span>

<span data-ttu-id="01ec2-106">Cette section traite trois aspects principaux des performances du serveur RPC :</span><span class="sxs-lookup"><span data-stu-id="01ec2-106">This section addresses three primary aspects of RPC server performance:</span></span>

-   [<span data-ttu-id="01ec2-107">Latence et débit du réseau</span><span class="sxs-lookup"><span data-stu-id="01ec2-107">Network Latency and Throughput</span></span>](network-latency-and-throughput.md)
-   [<span data-ttu-id="01ec2-108">Extensibilité</span><span class="sxs-lookup"><span data-stu-id="01ec2-108">Scalability</span></span>](scalability.md)
-   [<span data-ttu-id="01ec2-109">Conseils sur les performances des appels RPC divers</span><span class="sxs-lookup"><span data-stu-id="01ec2-109">Miscellaneous RPC Performance Tips</span></span>](miscellaneous-rpc-performance-tips.md)

<span data-ttu-id="01ec2-110">La longueur du chemin d’accès du code est un autre facteur de performance principal pour RPC.</span><span class="sxs-lookup"><span data-stu-id="01ec2-110">Code path length is another primary performance consideration for RPC.</span></span> <span data-ttu-id="01ec2-111">La longueur du chemin de code est généralement bien comprise, et dans la mesure où la documentation et les outils sont largement disponibles sur ce sujet, cet article ne traite pas de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="01ec2-111">Code path length is generally well understood, and since literature and tools are widely available on that topic, this article does not address it.</span></span>

<span data-ttu-id="01ec2-112">Une règle de performance générale importante et établie à retenir lors de l’examen des performances RPC est la suivante : Rechercher le goulot d’étranglement dans le système et travailler pour le résoudre.</span><span class="sxs-lookup"><span data-stu-id="01ec2-112">An important and established general performance rule to remember while considering RPC performance is this: find the bottleneck in the system, and work to resolve that.</span></span> <span data-ttu-id="01ec2-113">Le goulet d’étranglement de la passerelle peut ne pas être la programmation RPC et, si tel est le cas, le réglage des performances dans RPC n’entraîne pas de performances améliorées tant que ce goulot d’étranglement n’est pas traité.</span><span class="sxs-lookup"><span data-stu-id="01ec2-113">The gating bottleneck may not be the RPC programming, and if that is the case, performance tuning in RPC will not result in enhanced performance until that bottleneck is addressed.</span></span> <span data-ttu-id="01ec2-114">Par exemple, il n’est pas nécessaire d’utiliser le réseau par le biais d’une contention de ressources.</span><span class="sxs-lookup"><span data-stu-id="01ec2-114">For example, a system plagued by resource contention does not need to make more efficient use of the network.</span></span>

<span data-ttu-id="01ec2-115">Si votre système est déployé dans différents environnements, il est judicieux de s’assurer que tous les aspects sont bien réglés, dans la mesure où différents environnements peuvent produire des goulots d’étranglement de performances variés.</span><span class="sxs-lookup"><span data-stu-id="01ec2-115">If your system is deployed in various environments, it is a good idea to make sure all aspects of it are well tuned, as different environments can produce varied performance bottlenecks.</span></span>

 

 