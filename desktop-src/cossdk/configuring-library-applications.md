---
description: Configuration des applications de bibliothèque
ms.assetid: db375e0f-74ca-44df-918a-b0e48742a594
title: Configuration des applications de bibliothèque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51e00626d42044797881ccb86553ddfda38a089
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033635"
---
# <a name="configuring-library-applications"></a><span data-ttu-id="b172f-103">Configuration des applications de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b172f-103">Configuring Library Applications</span></span>

<span data-ttu-id="b172f-104">Étant donné que les applications de bibliothèque COM+ s’exécutent dans le processus du client, les éléments configurables pour les applications de bibliothèque sont considérablement différents de ceux des applications serveur.</span><span class="sxs-lookup"><span data-stu-id="b172f-104">Because COM+ library applications run in the client's process, the configurable elements for library applications are considerably different than for server applications.</span></span> <span data-ttu-id="b172f-105">Vous ne pouvez pas configurer les aspects de l’application qui sont déterminés par le processus d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="b172f-105">You cannot configure any aspect of the application that is determined by the hosting process.</span></span>

<span data-ttu-id="b172f-106">Au niveau de l’application, plusieurs paramètres sont soit limités, soit indisponibles pour les applications de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b172f-106">At the application level, several settings are either limited or unavailable for library applications.</span></span> <span data-ttu-id="b172f-107">Ces contraintes sont décrites dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="b172f-107">These constraints are described in the following table:</span></span>



| <span data-ttu-id="b172f-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="b172f-108">Attribute</span></span>                                       | <span data-ttu-id="b172f-109">Description</span><span class="sxs-lookup"><span data-stu-id="b172f-109">Description</span></span>                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b172f-110">Niveau de sécurité</span><span class="sxs-lookup"><span data-stu-id="b172f-110">Security level</span></span><br/>                       | <span data-ttu-id="b172f-111">Vous devez choisir les contrôles d’accès au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="b172f-111">You must choose component-level access checks.</span></span> <span data-ttu-id="b172f-112">L’application de bibliothèque ne peut pas influencer les contrôles d’accès au niveau du processus.</span><span class="sxs-lookup"><span data-stu-id="b172f-112">The library application cannot influence process-level access checks.</span></span> <span data-ttu-id="b172f-113">Consultez [définition d’un niveau de sécurité pour les vérifications d’accès](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="b172f-113">See [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span><br/>             |
| <span data-ttu-id="b172f-114">Activation ou désactivation de l’authentification</span><span class="sxs-lookup"><span data-stu-id="b172f-114">Enabling or disabling authentication</span></span><br/> | <span data-ttu-id="b172f-115">Vous pouvez indiquer si l’application de bibliothèque doit participer à l’authentification effectuée par le processus hôte.</span><span class="sxs-lookup"><span data-stu-id="b172f-115">You can indicate whether the library application will participate in authentication performed by the host process.</span></span> <span data-ttu-id="b172f-116">Consultez [activation de l’authentification pour une application de bibliothèque](enabling-authentication-for-a-library-application.md).</span><span class="sxs-lookup"><span data-stu-id="b172f-116">See [Enabling Authentication for a Library Application](enabling-authentication-for-a-library-application.md).</span></span><br/> |
| <span data-ttu-id="b172f-117">Niveau d'emprunt d'identité</span><span class="sxs-lookup"><span data-stu-id="b172f-117">Impersonation level</span></span><br/>                  | <span data-ttu-id="b172f-118">Pas disponible.</span><span class="sxs-lookup"><span data-stu-id="b172f-118">Unavailable.</span></span> <span data-ttu-id="b172f-119">Le paramètre du processus hôte est utilisé.</span><span class="sxs-lookup"><span data-stu-id="b172f-119">The setting of the host process is used.</span></span> <br/>                                                                                                                                                                             |
| <span data-ttu-id="b172f-120">Identité de sécurité</span><span class="sxs-lookup"><span data-stu-id="b172f-120">Security identity</span></span><br/>                    | <span data-ttu-id="b172f-121">Pas disponible.</span><span class="sxs-lookup"><span data-stu-id="b172f-121">Unavailable.</span></span> <span data-ttu-id="b172f-122">L’application s’exécute sous l’identité du processus hôte.</span><span class="sxs-lookup"><span data-stu-id="b172f-122">The application runs under the identity of the host process.</span></span><br/>                                                                                                                                                          |
| <span data-ttu-id="b172f-123">Arrêt du processus serveur</span><span class="sxs-lookup"><span data-stu-id="b172f-123">Server process shutdown</span></span><br/>              | <span data-ttu-id="b172f-124">Pas disponible.</span><span class="sxs-lookup"><span data-stu-id="b172f-124">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="b172f-125">Activer la prise en charge de 3 Go</span><span class="sxs-lookup"><span data-stu-id="b172f-125">Enable 3-GB support</span></span><br/>                  | <span data-ttu-id="b172f-126">Pas disponible.</span><span class="sxs-lookup"><span data-stu-id="b172f-126">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="b172f-127">Lancer dans le débogueur</span><span class="sxs-lookup"><span data-stu-id="b172f-127">Launch in debugger</span></span><br/>                   | <span data-ttu-id="b172f-128">Pas disponible.</span><span class="sxs-lookup"><span data-stu-id="b172f-128">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="b172f-129">Activer CRM</span><span class="sxs-lookup"><span data-stu-id="b172f-129">Enable CRM</span></span><br/>                           | <span data-ttu-id="b172f-130">Pas disponible.</span><span class="sxs-lookup"><span data-stu-id="b172f-130">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="b172f-131">Queuing</span><span class="sxs-lookup"><span data-stu-id="b172f-131">Queuing</span></span><br/>                              | <span data-ttu-id="b172f-132">Pas disponible.</span><span class="sxs-lookup"><span data-stu-id="b172f-132">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="b172f-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b172f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b172f-134">Vue d’ensemble de l’application COM+</span><span class="sxs-lookup"><span data-stu-id="b172f-134">COM+ Application Overview</span></span>](com--application-overview.md)
</dt> </dl>

 

 




