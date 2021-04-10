---
title: Composants RPC
description: Composants d’appel de procédure distante (RPC).
ms.assetid: 7caaf01a-7f20-470f-afcf-478146cae5eb
keywords:
- Appel de procédure distante RPC, décrit, composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c715a4f454ef28db20ee527e5e8f33f66200b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940018"
---
# <a name="rpc-components"></a><span data-ttu-id="dbb57-104">Composants RPC</span><span class="sxs-lookup"><span data-stu-id="dbb57-104">RPC Components</span></span>

<span data-ttu-id="dbb57-105">RPC comprend les composants principaux suivants :</span><span class="sxs-lookup"><span data-stu-id="dbb57-105">RPC includes the following major components:</span></span>

-   <span data-ttu-id="dbb57-106">Compilateur MIDL</span><span class="sxs-lookup"><span data-stu-id="dbb57-106">MIDL compiler</span></span>
-   <span data-ttu-id="dbb57-107">Bibliothèques Runtime et fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="dbb57-107">Run-time libraries and header files</span></span>
-   <span data-ttu-id="dbb57-108">Fournisseur de services de noms (parfois appelé Localisateur)</span><span class="sxs-lookup"><span data-stu-id="dbb57-108">Name service provider (sometimes referred to as the Locator)</span></span>
-   <span data-ttu-id="dbb57-109">Mappeur de point de terminaison (parfois appelé mappeur de port)</span><span class="sxs-lookup"><span data-stu-id="dbb57-109">Endpoint mapper (sometimes referred to as the port mapper)</span></span>

<span data-ttu-id="dbb57-110">Dans le modèle RPC, vous pouvez spécifier formellement une interface aux procédures distantes à l’aide d’un langage conçu à cet effet.</span><span class="sxs-lookup"><span data-stu-id="dbb57-110">In the RPC model, you can formally specify an interface to the remote procedures using a language designed for this purpose.</span></span> <span data-ttu-id="dbb57-111">Cette langue est appelée IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="dbb57-111">This language is called the Interface Definition Language, or IDL.</span></span> <span data-ttu-id="dbb57-112">L’implémentation Microsoft de ce langage est appelée Microsoft Interface Definition Language, ou MIDL.</span><span class="sxs-lookup"><span data-stu-id="dbb57-112">The Microsoft implementation of this language is called the Microsoft Interface Definition Language, or MIDL.</span></span>

<span data-ttu-id="dbb57-113">Après avoir créé une interface, vous devez la passer par le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="dbb57-113">After you create an interface, you must pass it through the MIDL compiler.</span></span> <span data-ttu-id="dbb57-114">Ce compilateur génère les stubs qui traduisent les appels de procédure locale en appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="dbb57-114">This compiler generates the stubs that translate local procedure calls into remote procedure calls.</span></span> <span data-ttu-id="dbb57-115">Les stubs sont des fonctions d’espace réservé qui effectuent des appels aux fonctions de la bibliothèque Runtime, qui gèrent l’appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="dbb57-115">Stubs are placeholder functions that make the calls to the run-time library functions, which manage the remote procedure call.</span></span> <span data-ttu-id="dbb57-116">L’avantage de cette approche est que le réseau devient presque complètement transparent pour votre application distribuée.</span><span class="sxs-lookup"><span data-stu-id="dbb57-116">The advantage of this approach is that the network becomes almost completely transparent to your distributed application.</span></span> <span data-ttu-id="dbb57-117">Votre programme client appelle ce qui semble être une procédure locale ; la tâche de les transformer en appels distants est effectuée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="dbb57-117">Your client program calls what appear to be local procedures; the work of turning them into remote calls is done for you automatically.</span></span> <span data-ttu-id="dbb57-118">Tout le code qui traduit des données, accède au réseau et récupère les résultats est généré pour vous par le compilateur MIDL et est invisible pour votre application.</span><span class="sxs-lookup"><span data-stu-id="dbb57-118">All the code that translates data, accesses the network, and retrieves results is generated for you by the MIDL compiler and is invisible to your application.</span></span>

 

 




