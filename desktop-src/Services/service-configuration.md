---
description: Le système utilise les informations de configuration pour déterminer comment démarrer le service.
ms.assetid: fc8c631e-076c-4745-8db0-90f46a202e6a
title: Configuration du service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5019469e17fdd0807aa101c7d1e4d6f6019da783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525822"
---
# <a name="service-configuration"></a><span data-ttu-id="08a7f-103">Configuration du service</span><span class="sxs-lookup"><span data-stu-id="08a7f-103">Service Configuration</span></span>

<span data-ttu-id="08a7f-104">Le système utilise les informations de configuration pour déterminer comment démarrer le service.</span><span class="sxs-lookup"><span data-stu-id="08a7f-104">The system uses the configuration information to determine how to start the service.</span></span> <span data-ttu-id="08a7f-105">Les informations de configuration incluent également le nom complet du service et sa description.</span><span class="sxs-lookup"><span data-stu-id="08a7f-105">The configuration information also includes the service display name and its description.</span></span> <span data-ttu-id="08a7f-106">Par exemple, pour le service DHCP, vous pouvez utiliser le nom d’affichage « service Dynamic Host Configuration Protocol » et la description « fournit des adresses Internet pour l’ordinateur sur votre réseau ».</span><span class="sxs-lookup"><span data-stu-id="08a7f-106">For example, for the DHCP service, you could use the display name "Dynamic Host Configuration Protocol Service" and the description "Provides internet addresses for computer on your network."</span></span>

<span data-ttu-id="08a7f-107">Pour modifier les informations de configuration d’un objet de service, un programme de configuration utilise la fonction [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) ou [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) .</span><span class="sxs-lookup"><span data-stu-id="08a7f-107">To modify the configuration information for a service object, a configuration program uses the [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) or [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) function.</span></span> <span data-ttu-id="08a7f-108">Pour obtenir un exemple, consultez [modification d’une configuration de service](changing-a-service-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="08a7f-108">For an example, see [Changing a Service Configuration](changing-a-service-configuration.md).</span></span>

<span data-ttu-id="08a7f-109">Pour récupérer les informations de configuration d’un objet de service, le programme de configuration utilise la fonction [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) ou [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) .</span><span class="sxs-lookup"><span data-stu-id="08a7f-109">To retrieve the configuration information for a service object, the configuration program uses the [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) or [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) function.</span></span> <span data-ttu-id="08a7f-110">Pour obtenir un exemple, consultez [interrogation de la configuration d’un service](querying-a-service-s-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="08a7f-110">For an example, see [Querying a Service's Configuration](querying-a-service-s-configuration.md).</span></span>

<span data-ttu-id="08a7f-111">Les fonctions de configuration du service [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) et [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) prennent en charge l’utilisation de déclencheurs pour contrôler le démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="08a7f-111">The [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) and [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) service configuration functions support the use of triggers to control service start.</span></span>

<span data-ttu-id="08a7f-112">Pour modifier le descripteur de sécurité pour un objet SCManager ou un objet de service, un programme de configuration utilise la fonction [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) .</span><span class="sxs-lookup"><span data-stu-id="08a7f-112">To modify the security descriptor for either an SCManager object or a service object, a configuration program uses the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function.</span></span> <span data-ttu-id="08a7f-113">Pour récupérer une copie du descripteur de sécurité, le programme de configuration utilise la fonction [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) .</span><span class="sxs-lookup"><span data-stu-id="08a7f-113">To retrieve a copy of the security descriptor, the configuration program uses the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08a7f-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="08a7f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08a7f-115">Configuration d’un service à l’aide de SC</span><span class="sxs-lookup"><span data-stu-id="08a7f-115">Configuring a Service Using SC</span></span>](configuring-a-service-using-sc.md)
</dt> </dl>

 

 
