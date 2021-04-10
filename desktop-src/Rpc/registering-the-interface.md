---
title: Inscription de l’interface
description: L’inscription de l’interface qu’un programme serveur prend en charge permet aux appels de procédure distante provenant de programmes clients d’être distribués à la routine de serveur appropriée.
ms.assetid: 953185a7-00e6-442d-b474-a983f4a91c38
keywords:
- Appel de procédure distante RPC, tâches, inscription de l’interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a12de37b39c719de246ceb79a92d6a51fc361
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190730"
---
# <a name="registering-the-interface"></a><span data-ttu-id="0af2b-104">Inscription de l’interface</span><span class="sxs-lookup"><span data-stu-id="0af2b-104">Registering the Interface</span></span>

<span data-ttu-id="0af2b-105">L’inscription de l’interface qu’un programme serveur prend en charge permet aux appels de procédure distante provenant de programmes clients d’être distribués à la routine de serveur appropriée.</span><span class="sxs-lookup"><span data-stu-id="0af2b-105">Registering the interface that a server program supports enables remote procedure calls from client programs to be dispatched to the proper server routine.</span></span> <span data-ttu-id="0af2b-106">Les programmes serveur appellent [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) pour inscrire leurs interfaces.</span><span class="sxs-lookup"><span data-stu-id="0af2b-106">Server programs call [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) to register their interfaces.</span></span> <span data-ttu-id="0af2b-107">Le fragment de code suivant illustre son utilisation :</span><span class="sxs-lookup"><span data-stu-id="0af2b-107">The following code fragment demonstrates its use:</span></span>


```C++
RPC_STATUS status;
status = RpcServerRegisterIf(MyInterface_v1_0_s_ifspec, NULL, NULL);
```



<span data-ttu-id="0af2b-108">Le premier paramètre de la fonction [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) est une structure que le compilateur MIDL génère à partir du fichier IDL qui définit l’interface (ou les interfaces) du serveur.</span><span class="sxs-lookup"><span data-stu-id="0af2b-108">The first parameter to the [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) function is a structure the MIDL compiler generates from the IDL file that defines the interface (or interfaces) for the server.</span></span> <span data-ttu-id="0af2b-109">Les deuxième et troisième paramètres sont respectivement un UUID et un vecteur de point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0af2b-109">The second and third parameters are a UUID and an entry-point vector, respectively.</span></span> <span data-ttu-id="0af2b-110">Ils ont la valeur **null** dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="0af2b-110">They are set to **NULL** in this example.</span></span> <span data-ttu-id="0af2b-111">Dans de nombreux cas, votre programme serveur définira ces valeurs de paramètre sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="0af2b-111">In many instances, your server program will set these parameter values to **NULL**.</span></span> <span data-ttu-id="0af2b-112">Les programmes serveur utilisent le deuxième et le troisième paramètres lorsqu’ils fournissent plusieurs implémentations des mêmes procédures dans une interface.</span><span class="sxs-lookup"><span data-stu-id="0af2b-112">Server programs use the second and third parameters when they provide multiple implementations of the same procedures in an interface.</span></span> <span data-ttu-id="0af2b-113">Pour plus d’informations, consultez [vecteurs de point d’entrée](registering-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="0af2b-113">For more information, see [Entry-Point Vectors](registering-interfaces.md).</span></span>

<span data-ttu-id="0af2b-114">Les programmes serveur peuvent également utiliser [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) pour inscrire une interface.</span><span class="sxs-lookup"><span data-stu-id="0af2b-114">Server programs can also use [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) to register an interface.</span></span> <span data-ttu-id="0af2b-115">L’un des avantages de cette fonction est qu’elle offre à votre application la possibilité de définir une fonction de rappel de sécurité.</span><span class="sxs-lookup"><span data-stu-id="0af2b-115">One advantage of using this function is that it provides your application with the ability to set a security-callback function.</span></span> <span data-ttu-id="0af2b-116">L’utilisation des fonctions de rappel de sécurité est l’approche recommandée pour sécuriser une interface.</span><span class="sxs-lookup"><span data-stu-id="0af2b-116">Using security-callback functions is the recommended approach to securing an interface.</span></span>

> [!Note]  
> <span data-ttu-id="0af2b-117">MIDL produit deux structures très similaires, une pour le client et une pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="0af2b-117">MIDL produces two very similar structures, one for the client and one for the server.</span></span> <span data-ttu-id="0af2b-118">La structure transmise à la fonction [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) est la version serveur de la structure générée par MIDL.</span><span class="sxs-lookup"><span data-stu-id="0af2b-118">The structure passed to the [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) function is the server version of the MIDL-produced structure.</span></span>

 

 

 




