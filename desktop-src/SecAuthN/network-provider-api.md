---
description: Un fournisseur réseau est une DLL qui permet au système d’exploitation Windows d’interagir avec d’autres types de réseaux, tels que Novell. Il s’agit d’un client du pilote Windows WNet.
ms.assetid: d316f159-4fe3-4b78-9efc-177906875918
title: API du fournisseur réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc68184f60639a603614cbaf71631a2521012cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536543"
---
# <a name="network-provider-api"></a><span data-ttu-id="1980e-104">API du fournisseur réseau</span><span class="sxs-lookup"><span data-stu-id="1980e-104">Network Provider API</span></span>

<span data-ttu-id="1980e-105">Un fournisseur réseau est une DLL qui permet au système d’exploitation Windows d’interagir avec d’autres types de réseaux, tels que Novell.</span><span class="sxs-lookup"><span data-stu-id="1980e-105">A network provider is a DLL that enables the Windows operating system to interact with other kinds of networks, such as Novell.</span></span> <span data-ttu-id="1980e-106">Il s’agit d’un client du pilote Windows WNet.</span><span class="sxs-lookup"><span data-stu-id="1980e-106">It is a client of the Windows WNet driver.</span></span> <span data-ttu-id="1980e-107">Un fournisseur de réseau implémente des actions spécifiques au réseau, telles que l’établissement d’une connexion, et expose une interface commune à Windows.</span><span class="sxs-lookup"><span data-stu-id="1980e-107">A network provider implements network-specific actions, such as making a connection, and exposes a common interface to Windows.</span></span> <span data-ttu-id="1980e-108">Cette interface est appelée API du fournisseur réseau et est constituée de fonctions implémentées par le fournisseur réseau.</span><span class="sxs-lookup"><span data-stu-id="1980e-108">This interface is called the Network Provider API and consists of functions implemented by the network provider.</span></span> <span data-ttu-id="1980e-109">Vous pouvez créer une DLL de fournisseur réseau pour prendre en charge de nouveaux protocoles réseau.</span><span class="sxs-lookup"><span data-stu-id="1980e-109">You can create a network provider DLL to support new network protocols.</span></span>

<span data-ttu-id="1980e-110">Étant donné que chaque réseau expose une interface commune par le biais de son fournisseur, Windows peut interagir avec plusieurs types de réseaux sans connaître les détails de l’implémentation propre au réseau.</span><span class="sxs-lookup"><span data-stu-id="1980e-110">Because each network exposes a common interface through its provider, Windows can interact with several types of networks without knowing their network-specific implementation details.</span></span>

<span data-ttu-id="1980e-111">Le [*routeur de fournisseur multiple*](../secgloss/m-gly.md) (MPR) gère la communication avec tous les différents fournisseurs de réseau sur le système et présente un réseau intégré à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1980e-111">The [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) handles communication with all of the various network providers on the system and presents an integrated network to the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1980e-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1980e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1980e-113">Fournisseurs de réseau</span><span class="sxs-lookup"><span data-stu-id="1980e-113">Network Providers</span></span>](network-providers.md)
</dt> <dt>

[<span data-ttu-id="1980e-114">Gestionnaire d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="1980e-114">Credential Manager</span></span>](credential-manager.md)
</dt> <dt>

[<span data-ttu-id="1980e-115">Routeur à plusieurs fournisseurs</span><span class="sxs-lookup"><span data-stu-id="1980e-115">Multiple Provider Router</span></span>](multiple-provider-router.md)
</dt> <dt>

[<span data-ttu-id="1980e-116">Fonctions implémentées par les fournisseurs de réseau</span><span class="sxs-lookup"><span data-stu-id="1980e-116">Functions Implemented by Network Providers</span></span>](functions-implemented-by-network-providers.md)
</dt> <dt>

[<span data-ttu-id="1980e-117">API de gestion des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="1980e-117">Credential Management API</span></span>](credential-management-api.md)
</dt> <dt>

[<span data-ttu-id="1980e-118">API de notification de connexion</span><span class="sxs-lookup"><span data-stu-id="1980e-118">Connection Notification API</span></span>](connection-notification-api.md)
</dt> </dl>

 

 
