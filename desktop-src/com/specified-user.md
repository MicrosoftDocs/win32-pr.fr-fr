---
title: Utilisateur spécifié
description: Utilisateur spécifié
ms.assetid: ec7684fb-a9f1-4ef2-a7d4-07caf24b6023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acce63aa502a8966cd0eb53c90dcca3c4454e80b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106532026"
---
# <a name="specified-user"></a><span data-ttu-id="f30f1-103">Utilisateur spécifié</span><span class="sxs-lookup"><span data-stu-id="f30f1-103">Specified User</span></span>

<span data-ttu-id="f30f1-104">La spécification d’un utilisateur particulier (et du mot de passe de l’utilisateur) est l’identité par défaut pour les serveurs COM.</span><span class="sxs-lookup"><span data-stu-id="f30f1-104">Specifying a particular user (and the user's password) is the preferred identity for COM servers.</span></span> <span data-ttu-id="f30f1-105">La raison pour laquelle cette identité est privilégiée est que personne ne doit être connecté sur l’ordinateur sur lequel le serveur est en cours d’exécution et que chaque client communique avec la même instance du serveur si le serveur inscrit sa fabrique de classes en tant qu’utilisation multiple.</span><span class="sxs-lookup"><span data-stu-id="f30f1-105">The reason this identity is preferred is that no one has to be logged on the machine where the server is running for the server to run, and every client talks to the same instance of the server if the server registers its class factory as multi-use.</span></span> <span data-ttu-id="f30f1-106">Si le serveur dispose d’une interface utilisateur graphique, vous ne devez pas choisir cette identité ; Si vous le faites, l’utilisateur ne sera pas en mesure de voir l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f30f1-106">If the server has a GUI, you should not choose this identity; if you do, the user will not be able to see the user interface.</span></span>

<span data-ttu-id="f30f1-107">Ce type de serveur dispose d’un jeton principal et peut accéder aux ressources distantes dans lesquelles il est possible qu’un serveur qui a l’identité de lancement de l’utilisateur ne puisse pas.</span><span class="sxs-lookup"><span data-stu-id="f30f1-107">This type of server has a primary token and can access remote resources where a server that has the launching-user identity might not be able to.</span></span> <span data-ttu-id="f30f1-108">Pour plus d’informations sur l’emprunt d’identité et les jetons d’accès, consultez [niveaux d’emprunt d’identité](impersonation-levels.md) et [masquage](cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="f30f1-108">For more information about impersonation and access tokens, see [Impersonation Levels](impersonation-levels.md) and [Cloaking](cloaking.md).</span></span>

<span data-ttu-id="f30f1-109">L’exécution en tant que compte d’utilisateur fixe est plus sécurisée que l’identité de l’utilisateur interactif, car cette identité ne peut être affectée à l’application que par une personne qui a le mot de passe de l’utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="f30f1-109">Running as a fixed user account is more secure than the interactive user identity because this identity can be assigned to the application only by someone who has the specific user's password.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f30f1-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f30f1-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f30f1-111">Identité de l’application</span><span class="sxs-lookup"><span data-stu-id="f30f1-111">Application Identity</span></span>](application-identity.md)
</dt> <dt>

[<span data-ttu-id="f30f1-112">Utilisateur interactif</span><span class="sxs-lookup"><span data-stu-id="f30f1-112">Interactive User</span></span>](interactive-user.md)
</dt> <dt>

[<span data-ttu-id="f30f1-113">Lancement de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="f30f1-113">Launching User</span></span>](launching-user.md)
</dt> <dt>

[<span data-ttu-id="f30f1-114">Identité du service</span><span class="sxs-lookup"><span data-stu-id="f30f1-114">Service Identity</span></span>](service-identity.md)
</dt> </dl>

 

 




