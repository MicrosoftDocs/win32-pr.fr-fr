---
title: API du plug-in WinRM
description: L’interface de programmation d’applications (API) du plug-in WinRM fournit des fonctionnalités qui permettent à un utilisateur d’écrire des plug-ins en implémentant certaines API pour les opérations et URI de ressources pris en charge.
ms.assetid: d3e103c1-221b-441b-8bcb-883e3f2a4c1a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccc8920f7df788b4df355b0cbc23478e97111d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940121"
---
# <a name="winrm-plug-in-api"></a><span data-ttu-id="2d999-103">API du plug-in WinRM</span><span class="sxs-lookup"><span data-stu-id="2d999-103">WinRM Plug-in API</span></span>

<span data-ttu-id="2d999-104">Les plug-ins Windows Remote Management sont des bibliothèques de liens dynamiques (dll) natives qui s’y connectent et étendent les fonctionnalités de WinRM.</span><span class="sxs-lookup"><span data-stu-id="2d999-104">Windows Remote Management plug-ins are native dynamic-link libraries (DLLs) that plug into and extend the functionality of WinRM.</span></span> <span data-ttu-id="2d999-105">L’interface de programmation d’applications (API) du plug-in WinRM fournit des fonctionnalités qui permettent à un utilisateur d’écrire des plug-ins en implémentant certaines API pour les opérations et [*URI de ressources*](windows-remote-management-glossary.md) pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2d999-105">The WinRM Plug-in application programming interface (API) provides functionality that enables a user to write plug-ins by implementing certain APIs for supported [*resource URIs*](windows-remote-management-glossary.md) and operations.</span></span> <span data-ttu-id="2d999-106">Une fois les plug-ins configurés pour le service WinRM ou Internet Information Services (IIS), ils sont chargés dans l’hôte WinRM ou l’hôte IIS, respectivement.</span><span class="sxs-lookup"><span data-stu-id="2d999-106">After the plug-ins are configured for either the WinRM service or Internet Information Services (IIS), they are loaded into the WinRM host or IIS host, respectively.</span></span> <span data-ttu-id="2d999-107">Les demandes distantes sont routées vers ces points d’entrée de plug-in pour effectuer des opérations.</span><span class="sxs-lookup"><span data-stu-id="2d999-107">Remote requests are routed to these plug-in entry points to carry out operations.</span></span>

<span data-ttu-id="2d999-108">La section informations de référence sur l’API du plug-in WinRM contient des informations détaillées sur les éléments d’API suivants :</span><span class="sxs-lookup"><span data-stu-id="2d999-108">The WinRM Plug-in API reference section contains detailed information about the following API elements:</span></span>

-   [<span data-ttu-id="2d999-109">Points d’entrée du plug-in d’autorisation</span><span class="sxs-lookup"><span data-stu-id="2d999-109">Authorization Plug-in Entry Points</span></span>](authorization-plug-in-entry-points.md)
-   [<span data-ttu-id="2d999-110">Méthodes de plug-in d’autorisation</span><span class="sxs-lookup"><span data-stu-id="2d999-110">Authorization Plug-in Methods</span></span>](authorization-plug-in-methods.md)
-   [<span data-ttu-id="2d999-111">Points d’entrée du plug-in opérations</span><span class="sxs-lookup"><span data-stu-id="2d999-111">Operations Plug-in Entry Points</span></span>](operations-plug-in-entry-points.md)
-   [<span data-ttu-id="2d999-112">Méthodes de plug-in Operations</span><span class="sxs-lookup"><span data-stu-id="2d999-112">Operations Plug-in Methods</span></span>](operations-plug-in-methods.md)
-   [<span data-ttu-id="2d999-113">Structures</span><span class="sxs-lookup"><span data-stu-id="2d999-113">Structures</span></span>](winrm-plug-in-api-structures.md)

 

 




