---
title: Inscription des points de terminaison
description: L’inscription du programme serveur dans le mappage des points de terminaison de l’ordinateur hôte du serveur permet aux programmes clients de déterminer le point de terminaison (généralement un port TCP/IP ou un canal nommé) vers lequel le programme serveur est à l’écoute.
ms.assetid: d09874f8-2b55-4af2-bfe1-8978301d6692
keywords:
- Appel de procédure distante RPC, tâches, inscrire des points de terminaison
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23e02aaae18a9d28b989d16850693a8a8f0678e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671085"
---
# <a name="registering-endpoints"></a><span data-ttu-id="867b1-104">Inscription des points de terminaison</span><span class="sxs-lookup"><span data-stu-id="867b1-104">Registering Endpoints</span></span>

<span data-ttu-id="867b1-105">L’inscription du programme serveur dans le mappage des points de terminaison de l’ordinateur hôte du serveur permet aux programmes clients de déterminer le point de terminaison (généralement un port TCP/IP ou un canal nommé) vers lequel le programme serveur est à l’écoute.</span><span class="sxs-lookup"><span data-stu-id="867b1-105">Registering the server program in the endpoint map of the server host computer enables client programs to determine which endpoint (usually a TCP/IP port or a named pipe) the server program is listening to.</span></span> <span data-ttu-id="867b1-106">Pour s’inscrire dans le mappage de point de terminaison du système hôte du serveur, un programme serveur appelle la fonction [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) comme indiqué dans le fragment de code suivant :</span><span class="sxs-lookup"><span data-stu-id="867b1-106">To register itself in the server host system's endpoint map, a server program calls the [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) function as shown in the following code fragment:</span></span>


```C++
// This example assumes that MyInterface_v1_0_s_ifspec is a valid data
// structure that represents the interface being registered. The 
// variable is a valid pointer to a binding vector.
RPC_STATUS status;
status = RpcEpRegister(
    MyInterface_v1_0_s_ifspec,
    rpcBindingVector,
    NULL,
    NULL);
```



<span data-ttu-id="867b1-107">Le premier paramètre de [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) est la structure qui représente l’interface.</span><span class="sxs-lookup"><span data-stu-id="867b1-107">The first parameter to [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) is the structure that represents the interface.</span></span> <span data-ttu-id="867b1-108">Vous pouvez le trouver dans le fichier d’en-tête que le compilateur MIDL a généré à partir de votre fichier MIDL pour cette application distribuée.</span><span class="sxs-lookup"><span data-stu-id="867b1-108">You can find it in the header file that the MIDL compiler generated from your MIDL file for this distributed application.</span></span> <span data-ttu-id="867b1-109">Consultez [développement de l’interface](developing-the-interface.md).</span><span class="sxs-lookup"><span data-stu-id="867b1-109">See [Developing the Interface](developing-the-interface.md).</span></span> <span data-ttu-id="867b1-110">Ensuite, **RpcEpRegister** a besoin que votre application passe un ensemble de handles de liaison stockés dans un vecteur de liaison.</span><span class="sxs-lookup"><span data-stu-id="867b1-110">Next, **RpcEpRegister** needs your application to pass a set of binding handles that are stored in a binding vector.</span></span>

<span data-ttu-id="867b1-111">Outre l’inscription des noms d’interface, votre application serveur peut également inscrire des UUID d’objet dans le mappage de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="867b1-111">In addition to registering interface names, your server application can also register object UUIDs in the endpoint map.</span></span> <span data-ttu-id="867b1-112">Dans cet exemple, il n’y a aucun UUID d’objet à inscrire, donc le troisième paramètre de [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) est défini sur **null**.</span><span class="sxs-lookup"><span data-stu-id="867b1-112">In this example, there are no object UUIDs to register, so the third parameter to [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) is set to **NULL**.</span></span>

<span data-ttu-id="867b1-113">Le dernier paramètre est une chaîne de commentaire.</span><span class="sxs-lookup"><span data-stu-id="867b1-113">The last parameter is a comment string.</span></span> <span data-ttu-id="867b1-114">Bien que la bibliothèque Runtime RPC n’utilise pas cette chaîne, il est recommandé de définir la chaîne, car elle améliore la facilité de gestion du système.</span><span class="sxs-lookup"><span data-stu-id="867b1-114">Although the RPC run-time library does not use this string, setting the string is recommended, as it improves manageability of the system.</span></span> <span data-ttu-id="867b1-115">Un administrateur système peut utiliser la chaîne pour détecter les ports utilisés par les applications, qui peuvent ensuite être utilisées pour déterminer les ports à gérer par les pare-feu.</span><span class="sxs-lookup"><span data-stu-id="867b1-115">A system administrator can use the string to detect which ports are used by which applications, which can then be used to determine which ports to be managed by firewalls.</span></span>

 

 




