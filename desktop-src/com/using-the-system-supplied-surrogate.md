---
title: Utilisation du substitut System-Supplied
description: Utilisation du substitut System-Supplied
ms.assetid: 6709e5e2-50e0-470f-b618-3d3043f6e180
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444cb94c5564a78ec5580ae8e7f781e91a8a9c15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311389"
---
# <a name="using-the-system-supplied-surrogate"></a><span data-ttu-id="4e00a-103">Utilisation du substitut System-Supplied</span><span class="sxs-lookup"><span data-stu-id="4e00a-103">Using the System-Supplied Surrogate</span></span>

<span data-ttu-id="4e00a-104">Pour utiliser le substitut fourni par le système pour votre serveur DLL, inscrivez la DLL en spécifiant une chaîne vide ou une valeur **null** pour la valeur [DllSurrogate](dllsurrogate.md) dans le registre.</span><span class="sxs-lookup"><span data-stu-id="4e00a-104">To use the system-supplied surrogate for your DLL server, register the DLL specifying an empty string or **NULL** for the [DllSurrogate](dllsurrogate.md) value in the registry.</span></span> <span data-ttu-id="4e00a-105">Lorsqu’une demande d’activation pour un serveur de DLL désigné est fournie à COM, COM lance le processus de substitution par défaut et la DLL demandée (en spécifiant le CLSID sur la ligne de commande de lancement en interne) en même temps pour éviter un appel séparé.</span><span class="sxs-lookup"><span data-stu-id="4e00a-105">When an activation request for a DLL server so designated comes to COM, COM launches the default surrogate process and the requested DLL (by specifying the CLSID on the launch command line internally) at the same time to avoid a separate call.</span></span> <span data-ttu-id="4e00a-106">(Pour plus d’informations sur l’exécution de plusieurs serveurs DLL dans un processus de substitution, consultez [partage de substitution](surrogate-sharing.md).)</span><span class="sxs-lookup"><span data-stu-id="4e00a-106">(For information on running more than one DLL server in a surrogate process, see [Surrogate Sharing](surrogate-sharing.md).)</span></span>

<span data-ttu-id="4e00a-107">L’implémentation par défaut du processus de substitution est un serveur Pseudo-COM de style de modèle thread mixte.</span><span class="sxs-lookup"><span data-stu-id="4e00a-107">The default implementation of the surrogate process is a mixed-threading model style pseudo-COM server.</span></span> <span data-ttu-id="4e00a-108">Lorsque plusieurs serveurs DLL sont chargés dans un seul processus de substitution, ce processus garantit que chaque serveur DLL est instancié à l’aide du modèle de thread spécifié dans le registre pour ce serveur.</span><span class="sxs-lookup"><span data-stu-id="4e00a-108">When multiple DLL servers are loaded into a single surrogate process, this process ensures that each DLL server is instantiated using the threading model specified in the registry for that server.</span></span> <span data-ttu-id="4e00a-109">Tous les serveurs à thread libre chargés sont regroupés dans le cloisonnement multithread, tandis que chaque serveur à threads cloisonnés réside dans un cloisonnement monothread.</span><span class="sxs-lookup"><span data-stu-id="4e00a-109">All loaded free-threaded servers will live together in the multithreaded apartment, while each apartment-threaded server will reside in a single-threaded apartment.</span></span> <span data-ttu-id="4e00a-110">Si un serveur DLL prend en charge les deux modèles de thread, COM choisit le multithreading.</span><span class="sxs-lookup"><span data-stu-id="4e00a-110">If a DLL server supports both threading models, COM will choose multithreading.</span></span>

<span data-ttu-id="4e00a-111">Ce processus de substitution est écrit de sorte que COM gère à la fois le déchargement des serveurs DLL et l’arrêt du processus de substitution.</span><span class="sxs-lookup"><span data-stu-id="4e00a-111">This surrogate process is written so that COM handles both the unloading of DLL servers and the terminating of the surrogate process.</span></span>

<span data-ttu-id="4e00a-112">Le substitut fourni par le système fonctionne très bien pour la plupart des développeurs, et est très facile à utiliser.</span><span class="sxs-lookup"><span data-stu-id="4e00a-112">The system-provided surrogate will work very well for most developers, as well as being very easy to use.</span></span> <span data-ttu-id="4e00a-113">Toutefois, les développeurs qui ont des considérations spéciales peuvent décider qu’un substitut personnalisé est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4e00a-113">However, those developers with special considerations may decide that a custom surrogate is necessary.</span></span> <span data-ttu-id="4e00a-114">Pour plus d’informations, consultez [écriture d’un substitut personnalisé](writing-a-custom-surrogate.md).</span><span class="sxs-lookup"><span data-stu-id="4e00a-114">For more information, see [Writing a Custom Surrogate](writing-a-custom-surrogate.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e00a-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4e00a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e00a-116">Substituts de DLL</span><span class="sxs-lookup"><span data-stu-id="4e00a-116">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> </dl>

 

 




