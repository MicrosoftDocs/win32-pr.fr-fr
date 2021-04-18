---
title: Substituts de DLL
description: Substituts de DLL
ms.assetid: fe30c0ae-1d19-4a5f-8ee3-8a5337c79c44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c3fcbd07b4c6317dfb6ac8ede772fc62035f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512278"
---
# <a name="dll-surrogates"></a><span data-ttu-id="ad388-103">Substituts de DLL</span><span class="sxs-lookup"><span data-stu-id="ad388-103">DLL Surrogates</span></span>

<span data-ttu-id="ad388-104">COM permet de créer des serveurs DLL qui peuvent être chargés dans un processus EXE de substitution.</span><span class="sxs-lookup"><span data-stu-id="ad388-104">COM makes it possible to create DLL servers that can be loaded into a surrogate EXE process.</span></span> <span data-ttu-id="ad388-105">Cela combine la facilité d’écriture des serveurs DLL avec les avantages de l’implémentation de l’exécutable.</span><span class="sxs-lookup"><span data-stu-id="ad388-105">This combines the ease of writing DLL servers with the benefits of executable implementation.</span></span> <span data-ttu-id="ad388-106">Les outils de développement comme Microsoft Visual Studio faciliter l’écriture de serveurs DLL, mais un serveur DLL en lui-même a des limites.</span><span class="sxs-lookup"><span data-stu-id="ad388-106">Development tools like Microsoft Visual Studio facilitate the writing of DLL servers, but a DLL server in itself has limits.</span></span> <span data-ttu-id="ad388-107">L’exécution du serveur de DLL dans un processus de substitution offre plusieurs avantages possibles :</span><span class="sxs-lookup"><span data-stu-id="ad388-107">Running the DLL server in a surrogate process offers several possible benefits:</span></span>

-   <span data-ttu-id="ad388-108">Isolation des erreurs et possibilité de traiter plusieurs clients simultanément.</span><span class="sxs-lookup"><span data-stu-id="ad388-108">Fault isolation and the ability to service multiple clients simultaneously.</span></span>
-   <span data-ttu-id="ad388-109">Dans un environnement distribué, une implémentation de serveur DLL peut être utilisée pour traiter les clients distants.</span><span class="sxs-lookup"><span data-stu-id="ad388-109">In a distributed environment, a DLL server implementation could be used to service remote clients.</span></span>
-   <span data-ttu-id="ad388-110">Cela peut permettre aux clients de se protéger eux-mêmes du code du serveur non approuvé tout en leur permettant d’accéder aux services fournis par le serveur de DLL.</span><span class="sxs-lookup"><span data-stu-id="ad388-110">It could permit clients to help protect themselves from untrusted server code while allowing them access to the services the DLL server provides.</span></span>
-   <span data-ttu-id="ad388-111">L’exécution d’un serveur DLL dans un substitut fournit la DLL avec la sécurité du substitut.</span><span class="sxs-lookup"><span data-stu-id="ad388-111">Running a DLL server in a surrogate provides the DLL with the surrogate's security.</span></span>

<span data-ttu-id="ad388-112">COM fournit un processus de substitution par défaut, ou vous pouvez écrire un substitut personnalisé si vous avez des besoins spéciaux.</span><span class="sxs-lookup"><span data-stu-id="ad388-112">COM provides a default surrogate process, or you can write a custom surrogate if you have special needs.</span></span>

<span data-ttu-id="ad388-113">Les rubriques suivantes fournissent plus d’informations sur les substituts de DLL :</span><span class="sxs-lookup"><span data-stu-id="ad388-113">The following topics provide more information on DLL surrogates:</span></span>

-   [<span data-ttu-id="ad388-114">Configuration requise du serveur DLL</span><span class="sxs-lookup"><span data-stu-id="ad388-114">DLL Server Requirements</span></span>](dll-server-requirements.md)
-   [<span data-ttu-id="ad388-115">Utilisation du substitut System-Supplied</span><span class="sxs-lookup"><span data-stu-id="ad388-115">Using the System-Supplied Surrogate</span></span>](using-the-system-supplied-surrogate.md)
-   [<span data-ttu-id="ad388-116">Écriture d’un substitut personnalisé</span><span class="sxs-lookup"><span data-stu-id="ad388-116">Writing a Custom Surrogate</span></span>](writing-a-custom-surrogate.md)

 

 




