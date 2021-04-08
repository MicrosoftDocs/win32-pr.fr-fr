---
title: Lancement de l’utilisateur
description: Lancement de l’utilisateur
ms.assetid: ea5140b6-0a79-4149-b845-4f6388e89104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6fb60652bff77eb27a33ec8a8a8d40db0f0023
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842766"
---
# <a name="launching-user"></a><span data-ttu-id="2a79f-103">Lancement de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="2a79f-103">Launching User</span></span>

<span data-ttu-id="2a79f-104">Il s’agit du paramètre par défaut pour l’identité de l’application.</span><span class="sxs-lookup"><span data-stu-id="2a79f-104">This is the default setting for the application identity.</span></span> <span data-ttu-id="2a79f-105">Lorsque l’utilisateur de lancement est choisi pour l’identité de l’application, chaque compte client obtient une nouvelle instance du serveur et chaque serveur reçoit sa propre [station Windows](/windows/desktop/winstation/window-stations).</span><span class="sxs-lookup"><span data-stu-id="2a79f-105">When the launching user is chosen for the application's identity, each client account gets a new instance of the server and each server gets its own [window station](/windows/desktop/winstation/window-stations).</span></span> <span data-ttu-id="2a79f-106">En raison des instances de serveur distinctes, le lancement de l’utilisateur est le paramètre d’identité de protection de sécurité de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="2a79f-106">Because of the separate server instances, launching user is the highest-level security protection identity setting.</span></span> <span data-ttu-id="2a79f-107">Toutefois, il existe des limites limitées sur la consommation des ressources.</span><span class="sxs-lookup"><span data-stu-id="2a79f-107">However, there are finite limits on resource consumption.</span></span> <span data-ttu-id="2a79f-108">En outre, toute interface utilisateur graphique affichée par le serveur n’est pas visible par le client.</span><span class="sxs-lookup"><span data-stu-id="2a79f-108">Also, any GUI the server displays will not be seen by the client.</span></span>

<span data-ttu-id="2a79f-109">Si l’application a l’identité de l’utilisateur de lancement, elle s’exécute avec un jeton d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="2a79f-109">If the application has the identity of the launching user, it runs with an impersonation token.</span></span> <span data-ttu-id="2a79f-110">Pour plus d’informations sur l’emprunt d’identité et les jetons d’accès, consultez [niveaux d’emprunt d’identité](impersonation-levels.md) et [masquage](cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="2a79f-110">For more information about impersonation and access tokens, see [Impersonation Levels](impersonation-levels.md) and [Cloaking](cloaking.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a79f-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2a79f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a79f-112">Identité de l’application</span><span class="sxs-lookup"><span data-stu-id="2a79f-112">Application Identity</span></span>](application-identity.md)
</dt> <dt>

[<span data-ttu-id="2a79f-113">Utilisateur interactif</span><span class="sxs-lookup"><span data-stu-id="2a79f-113">Interactive User</span></span>](interactive-user.md)
</dt> <dt>

[<span data-ttu-id="2a79f-114">Identité du service</span><span class="sxs-lookup"><span data-stu-id="2a79f-114">Service Identity</span></span>](service-identity.md)
</dt> <dt>

[<span data-ttu-id="2a79f-115">Utilisateur spécifié</span><span class="sxs-lookup"><span data-stu-id="2a79f-115">Specified User</span></span>](specified-user.md)
</dt> </dl>

 

 