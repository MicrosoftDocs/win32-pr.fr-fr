---
title: Méthodes de sécurité
description: Microsoft RPC prend en charge deux méthodes différentes pour l’ajout de la sécurité à votre application distribuée.
ms.assetid: 10dd8e71-668a-46bf-ab5d-e4b1e0e56a46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 367c4d052301ac1100d84cf18dc63e1540ed34b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029663"
---
# <a name="security-methods"></a><span data-ttu-id="479ba-103">Méthodes de sécurité</span><span class="sxs-lookup"><span data-stu-id="479ba-103">Security Methods</span></span>

<span data-ttu-id="479ba-104">Microsoft RPC prend en charge deux méthodes différentes pour l’ajout de la sécurité à votre application distribuée.</span><span class="sxs-lookup"><span data-stu-id="479ba-104">Microsoft RPC supports two different methods for adding security to your distributed application.</span></span> <span data-ttu-id="479ba-105">La première méthode consiste à utiliser l’interface SSPI (Security Support Provider Interface), accessible à l’aide des fonctions RPC.</span><span class="sxs-lookup"><span data-stu-id="479ba-105">The first method is to use the Security Support Provider Interface (SSPI), which can be accessed using the RPC functions.</span></span> <span data-ttu-id="479ba-106">En général, il est préférable d’utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="479ba-106">In general, it is best to use this method.</span></span> <span data-ttu-id="479ba-107">L’interface SSPI fournit les fonctionnalités d’authentification les plus flexibles et indépendantes du réseau.</span><span class="sxs-lookup"><span data-stu-id="479ba-107">The SSPI provides the most flexible and network-independent authentication features.</span></span>

<span data-ttu-id="479ba-108">La deuxième méthode consiste à utiliser les fonctionnalités de sécurité intégrées aux protocoles de transport système.</span><span class="sxs-lookup"><span data-stu-id="479ba-108">The second method is to use the security features built into the system transport protocols.</span></span> <span data-ttu-id="479ba-109">La méthode de sécurité au niveau du transport n’est pas la méthode recommandée.</span><span class="sxs-lookup"><span data-stu-id="479ba-109">The transport-level security method is not the preferred method.</span></span> <span data-ttu-id="479ba-110">L’utilisation de l’interface SSPI est recommandée car elle fonctionne sur tous les transports, sur plusieurs plateformes, et fournit des niveaux élevés de sécurité, notamment la confidentialité.</span><span class="sxs-lookup"><span data-stu-id="479ba-110">Using the SSPI is recommended because it works on all transports, across platforms, and provides high levels of security, including privacy.</span></span>

<span data-ttu-id="479ba-111">Cette section fournit des vues d’ensemble de la sécurité SSPI et de la sécurité au niveau du transport dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="479ba-111">This section provides overviews of both SSPI and transport-level security in the following topics:</span></span>

-   [<span data-ttu-id="479ba-112">interface du fournisseur de la prise en charge de la sécurité (Security Support Provider Interface ou SSPI)</span><span class="sxs-lookup"><span data-stu-id="479ba-112">Security Support Provider Interface (SSPI)</span></span>](security-support-provider-interface-sspi-.md)
-   [<span data-ttu-id="479ba-113">Sécurité de transport</span><span class="sxs-lookup"><span data-stu-id="479ba-113">Transport Security</span></span>](transport-security.md)

 

 




