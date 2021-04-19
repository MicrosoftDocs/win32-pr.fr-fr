---
title: Handles de liaison explicites
description: Pour un contrôle maximal sur le processus de liaison, les applications client/serveur peuvent utiliser des handles de liaison explicites.
ms.assetid: e711ce37-92f0-4e60-a126-148c27662c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b391c339ac3747928e3394152e9c0de7c1c7aa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510212"
---
# <a name="explicit-binding-handles"></a><span data-ttu-id="441bf-103">Handles de liaison explicites</span><span class="sxs-lookup"><span data-stu-id="441bf-103">Explicit Binding Handles</span></span>

<span data-ttu-id="441bf-104">Pour un contrôle maximal sur le processus de liaison, les applications client/serveur peuvent utiliser des handles de liaison explicites.</span><span class="sxs-lookup"><span data-stu-id="441bf-104">For maximum control over the binding process, client/server applications may use explicit binding handles.</span></span> <span data-ttu-id="441bf-105">À l’instar des handles implicites, les handles de liaison explicites permettent à votre application cliente de sélectionner un serveur pour exécuter ses appels.</span><span class="sxs-lookup"><span data-stu-id="441bf-105">Like implicit handles, explicit binding handles enable your client application to select a server to execute its calls.</span></span> <span data-ttu-id="441bf-106">En outre, les handles de liaison explicites permettent à votre application client/serveur de créer une session de communication RPC authentifiée.</span><span class="sxs-lookup"><span data-stu-id="441bf-106">In addition, explicit binding handles enable your client/server application to create an authenticated RPC communication session.</span></span> <span data-ttu-id="441bf-107">Avec les handles explicites, votre client peut se connecter à plusieurs serveurs et exécuter des procédures distantes sur plusieurs serveurs.</span><span class="sxs-lookup"><span data-stu-id="441bf-107">With explicit handles, your client can connect to more than one server and execute remote procedures on multiple servers.</span></span> <span data-ttu-id="441bf-108">Les applications clientes multithread et asynchrones peuvent même se connecter à plusieurs serveurs et exécuter plusieurs procédures distantes en même temps.</span><span class="sxs-lookup"><span data-stu-id="441bf-108">Multithreaded and asynchronous client applications can even connect to multiple servers and execute multiple remote procedures at the same time.</span></span>

<span data-ttu-id="441bf-109">Votre application cliente doit passer le handle explicite en tant que paramètre à chaque appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="441bf-109">Your client application must pass the explicit handle as a parameter to each remote procedure call.</span></span> <span data-ttu-id="441bf-110">Pour se conformer à la norme OSF, le descripteur doit être spécifié en tant que premier paramètre sur chaque procédure distante.</span><span class="sxs-lookup"><span data-stu-id="441bf-110">To conform to the OSF standard, the handle should be specified as the first parameter on each remote procedure.</span></span> <span data-ttu-id="441bf-111">Toutefois, les extensions Microsoft de RPC vous permettent de spécifier le descripteur de liaison dans d’autres positions.</span><span class="sxs-lookup"><span data-stu-id="441bf-111">However, the Microsoft extensions to RPC enable you to specify the binding handle in other positions.</span></span> <span data-ttu-id="441bf-112">Pour plus d’informations, consultez [Microsoft RPC Binding-Handle extensions](microsoft-rpc-binding-handle-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="441bf-112">For more information, see [Microsoft RPC Binding-Handle Extensions](microsoft-rpc-binding-handle-extensions.md).</span></span>

<span data-ttu-id="441bf-113">Pour créer un handle explicite, déclarez le descripteur en tant que paramètre pour les opérations distantes dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="441bf-113">To create an explicit handle, declare the handle as a parameter to the remote operations in the IDL file.</span></span> <span data-ttu-id="441bf-114">L' [exemple Hello, World](tutorial.md) peut être redéfini pour utiliser un handle explicite comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="441bf-114">The [Hello, World example](tutorial.md) can be redefined to use an explicit handle as shown:</span></span>

``` syntax
/* IDL file for explicit handles */
 
[ 
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0) 
]
interface hello
{
  void HelloProc([in] handle_t h1,
                 [in, string] char *  pszString); 
}
```

<span data-ttu-id="441bf-115">Vous pouvez combiner des handles explicites et implicites dans une seule interface.</span><span class="sxs-lookup"><span data-stu-id="441bf-115">You can combine explicit and implicit handles in a single interface.</span></span> <span data-ttu-id="441bf-116">Si une fonction a un handle explicite dans sa liste de paramètres, ce handle sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="441bf-116">If a function has an explicit handle in its parameter list, that handle will be used.</span></span> <span data-ttu-id="441bf-117">Si une fonction dans une interface utilisant des handles implicites ne spécifie pas de handle explicite, le handle implicite par défaut sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="441bf-117">If a function in an interface using implicit handles does not specify an explicit handle, then the default implicit handle will be used.</span></span>

 

 




