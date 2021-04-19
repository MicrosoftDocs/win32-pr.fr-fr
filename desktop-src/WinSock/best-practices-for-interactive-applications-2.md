---
description: Dans la transformation du code de mise à jour de la cellule de vie, plusieurs recommandations pour l’écriture d’applications réseau hautes performances ont été découvertes.
ms.assetid: 2c5d0610-88b5-437e-acde-214553121380
title: Meilleures pratiques pour les applications interactives
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89764cf19de223f4622edd947c8122bc7fe8b11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538641"
---
# <a name="best-practices-for-interactive-applications"></a><span data-ttu-id="cca51-103">Meilleures pratiques pour les applications interactives</span><span class="sxs-lookup"><span data-stu-id="cca51-103">Best Practices for Interactive Applications</span></span>

<span data-ttu-id="cca51-104">Dans la transformation du code de mise à jour de la cellule de vie, plusieurs recommandations pour l’écriture d’applications réseau hautes performances ont été découvertes.</span><span class="sxs-lookup"><span data-stu-id="cca51-104">In morphing the Life cell update code, several guidelines for writing high performance network applications have been uncovered.</span></span> <span data-ttu-id="cca51-105">Voici quelques stratégies générales à appliquer lors de l’écriture de ces types d’applications :</span><span class="sxs-lookup"><span data-stu-id="cca51-105">Some general strategies to apply when writing these types of applications are:</span></span>

-   <span data-ttu-id="cca51-106">Rendez le flux de données le plus possible, au lieu de passer en bloc.</span><span class="sxs-lookup"><span data-stu-id="cca51-106">Make the data stream as much as possible, rather than going in chunks.</span></span>
-   <span data-ttu-id="cca51-107">Utilisez quelques transactions de grande taille plutôt que plusieurs petites.</span><span class="sxs-lookup"><span data-stu-id="cca51-107">Use a few large transactions rather than many small ones.</span></span> <span data-ttu-id="cca51-108">Les transactions volumineuses peuvent également être diffusées de façon efficace.</span><span class="sxs-lookup"><span data-stu-id="cca51-108">Large transactions can also be efficiently streamed.</span></span>
-   <span data-ttu-id="cca51-109">Reconnaissez que le réseau est une ressource lente et peu fiable et développez chaque application pour réduire sa dépendance sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="cca51-109">Recognize that the network is a slow, unreliable resource and develop each application to minimize its reliance on the network.</span></span>
-   <span data-ttu-id="cca51-110">Utilisez une représentation bien structurée des données sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="cca51-110">Use a well-architected representation of the data on the network.</span></span> <span data-ttu-id="cca51-111">La représentation des données doit être indépendante de l’architecture de l’ordinateur, ne contenir aucun FAT et éventuellement être compressée.</span><span class="sxs-lookup"><span data-stu-id="cca51-111">The data representation should be computer-architecture agnostic, contain no fat, and possibly be compressed.</span></span>
-   <span data-ttu-id="cca51-112">Pendant l’initialisation et l’arrêt, ne laissez pas l’utilisateur attendre que le réseau démarre ou s’arrête.</span><span class="sxs-lookup"><span data-stu-id="cca51-112">During initialization and shutdown, do not make the user wait for the network to start up or shut down.</span></span> <span data-ttu-id="cca51-113">L’initialisation associée au réseau peut prendre beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="cca51-113">Network related initialization could take a relatively long time.</span></span> <span data-ttu-id="cca51-114">Séparez le code réseau non critique.</span><span class="sxs-lookup"><span data-stu-id="cca51-114">Separate the noncritical network code.</span></span>
-   <span data-ttu-id="cca51-115">Gérer les erreurs en fonction de leur impact.</span><span class="sxs-lookup"><span data-stu-id="cca51-115">Handle errors as appropriate to their impact.</span></span> <span data-ttu-id="cca51-116">Toutes les erreurs ne sont pas critiques.</span><span class="sxs-lookup"><span data-stu-id="cca51-116">Not all errors are critical.</span></span> <span data-ttu-id="cca51-117">Implémentez des mécanismes de récupération et fournissez des commentaires utilisateur non intrusifs.</span><span class="sxs-lookup"><span data-stu-id="cca51-117">Implement recovery mechanisms and provide nonintrusive user feedback.</span></span>
-   <span data-ttu-id="cca51-118">Utilisez des appels de procédure distante (RPC) uniquement lorsque cela est approprié.</span><span class="sxs-lookup"><span data-stu-id="cca51-118">Use remote procedure calls (RPC) only when appropriate.</span></span> <span data-ttu-id="cca51-119">RPC est synchrone sur Windows Me/98 et produit toujours des protocoles de conversation et FAT lorsqu’il est utilisé pour envoyer de petites quantités de données.</span><span class="sxs-lookup"><span data-stu-id="cca51-119">RPC is synchronous on Windows Me/98 and always results in chatty, fat protocols when used to send small amounts of data.</span></span>
-   <span data-ttu-id="cca51-120">Mesurez votre charge réseau à l’aide de netstat ; vous serez peut-être surpris de ce que vos mesures révèlent.</span><span class="sxs-lookup"><span data-stu-id="cca51-120">Measure your network overhead using Netstat; you may be surprised at what your measurements reveal.</span></span>
-   <span data-ttu-id="cca51-121">Testez l’application sur un grand nombre de réseaux, en particulier les réseaux lents ou susceptibles de nuire aux pertes.</span><span class="sxs-lookup"><span data-stu-id="cca51-121">Test the application on a variety of networks, especially slow or loss-prone networks.</span></span> <span data-ttu-id="cca51-122">Les réseaux locaux sans fil, les modems et les réseaux privés virtuels (VPN) sur Internet sont de bons réseaux à tester.</span><span class="sxs-lookup"><span data-stu-id="cca51-122">Wireless LAN networks, modems, and virtual private networks (VPN) over the Internet are good networks for testing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cca51-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cca51-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cca51-124">Applications Windows Sockets hautes performances</span><span class="sxs-lookup"><span data-stu-id="cca51-124">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



