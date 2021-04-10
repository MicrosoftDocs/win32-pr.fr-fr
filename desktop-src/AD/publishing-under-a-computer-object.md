---
title: Publication sous un objet ordinateur
description: En règle générale, les services basés sur l’hôte créent des SCP sous l’objet ordinateur pour l’ordinateur hôte. Les services basés sur l’hôte sont des services étroitement liés à un seul ordinateur hôte.
ms.assetid: ecd7d8bc-4714-408a-856c-7cab8360bf81
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fe382001910f3b78b4461c622e94b14c54fb59
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842038"
---
# <a name="publishing-under-a-computer-object"></a><span data-ttu-id="da9d0-104">Publication sous un objet ordinateur</span><span class="sxs-lookup"><span data-stu-id="da9d0-104">Publishing Under a Computer Object</span></span>

<span data-ttu-id="da9d0-105">En règle générale, les services basés sur l’hôte créent des SCP sous l’objet ordinateur pour l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="da9d0-105">Typically, host-based services create SCPs under the computer object for the host computer.</span></span> <span data-ttu-id="da9d0-106">Les services basés sur l’hôte sont des services étroitement liés à un seul ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="da9d0-106">Host-based services are services closely tied to a single host computer.</span></span>

<span data-ttu-id="da9d0-107">**Pour créer des SCP sous un objet ordinateur**</span><span class="sxs-lookup"><span data-stu-id="da9d0-107">**To create SCPs under a computer object**</span></span>

1.  <span data-ttu-id="da9d0-108">Appelez la fonction [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) pour obtenir le nom unique (DN) dans le répertoire de l’objet ordinateur de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="da9d0-108">Call the [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) function to get the distinguished name (DN) in the directory of the computer object for the local computer.</span></span>
2.  <span data-ttu-id="da9d0-109">Utilisez ce DN pour établir une liaison à l’objet ordinateur et créer le SCP.</span><span class="sxs-lookup"><span data-stu-id="da9d0-109">Use that DN to bind to the computer object and create the SCP.</span></span>

<span data-ttu-id="da9d0-110">Pour plus d’informations et pour obtenir un exemple de code, consultez [Comment les clients recherchent et utilisent un point de connexion de service](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="da9d0-110">For more information and a code example, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span>

<span data-ttu-id="da9d0-111">N’oubliez pas que seuls les ordinateurs membres du domaine disposent d’objets ordinateur valides dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="da9d0-111">Be aware that only domain-member computers have valid computer objects in the directory.</span></span>

<span data-ttu-id="da9d0-112">Pour récupérer le nom DNS ou NetBIOS de l’ordinateur local, appelez la fonction [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) .</span><span class="sxs-lookup"><span data-stu-id="da9d0-112">To get the DNS or NetBIOS name of the local computer, call the [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function.</span></span>

 

 