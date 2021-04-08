---
description: .
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: Microsoft Message Queuing (MSMQ)-suppression du service de support client Windows 2000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54688ee4ad24eb691c95e4d70ce0acb881e212eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035038"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a><span data-ttu-id="a13cc-103">Microsoft Message Queuing (MSMQ)-suppression du service de support client Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a13cc-103">Microsoft Message Queuing (MSMQ) - Removal of Windows 2000 Client Support Service</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="a13cc-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="a13cc-104">Affected Platforms</span></span>

<span data-ttu-id="a13cc-105">**Serveurs** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a13cc-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="a13cc-106">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="a13cc-106">Feature Impact</span></span>

 <span data-ttu-id="a13cc-107">**Gravité** -haute</span><span class="sxs-lookup"><span data-stu-id="a13cc-107">**Severity** - High</span></span>  
<span data-ttu-id="a13cc-108">**Fréquence** -faible</span><span class="sxs-lookup"><span data-stu-id="a13cc-108">**Frequency** - Low</span></span>  

## <a name="description"></a><span data-ttu-id="a13cc-109">Description</span><span class="sxs-lookup"><span data-stu-id="a13cc-109">Description</span></span>

<span data-ttu-id="a13cc-110">Le service de support client Windows 2000 est un composant facultatif du serveur Message Queuing que vous pouvez installer sur un ordinateur contrôleur de domaine Windows 2003 ou Windows 2008.</span><span class="sxs-lookup"><span data-stu-id="a13cc-110">The Windows 2000 Client Support Service is an optional component of the Message Queuing Server that you can install on a Windows 2003 or Windows 2008 domain controller machine.</span></span> <span data-ttu-id="a13cc-111">Ce service permet aux clients Windows 2000 de fonctionner en mode intégré au domaine, avec n’importe quel serveur Message Queuing installé sur les ordinateurs Windows 2003/2008.</span><span class="sxs-lookup"><span data-stu-id="a13cc-111">This service allows Windows 2000 clients to operate in a domain-integrated mode with any Message Queuing server installed on Windows 2003/2008 machines.</span></span> <span data-ttu-id="a13cc-112">Les clients MSMQ fonctionnant sur Windows XP vers le haut n’ont pas besoin de ce service.</span><span class="sxs-lookup"><span data-stu-id="a13cc-112">MSMQ Clients operating on Windows XP upwards do not need this service.</span></span>

### <a name="manifestation-of-impact"></a><span data-ttu-id="a13cc-113">Manifeste de l’impact</span><span class="sxs-lookup"><span data-stu-id="a13cc-113">Manifestation of Impact</span></span>

<span data-ttu-id="a13cc-114">Cette modification a un impact sur Windows 2000 lors de l’interopérabilité dans un domaine Windows 7 où tous les contrôleurs de domaine sont Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="a13cc-114">This change impacts Windows 2000 when interoperating in a Windows 7 domain where all domain controllers are Windows Server 2008 R2.</span></span> <span data-ttu-id="a13cc-115">Si un client est mis à niveau vers le domaine Windows 7, les applications MSMQ existantes sur les ordinateurs Windows 2000 dans le domaine ne pourront pas fonctionner en mode intégré au domaine, sauf si ces clients sont mis à niveau vers une version plus récente de Windows.</span><span class="sxs-lookup"><span data-stu-id="a13cc-115">If a customer upgrades to the Windows 7 domain, the existing MSMQ applications on any Windows 2000 machines in the domain will not be able to operate in a domain-integrated mode unless these clients upgrade to a higher Windows version.</span></span>

### <a name="mitigation"></a><span data-ttu-id="a13cc-116">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="a13cc-116">Mitigation</span></span>

<span data-ttu-id="a13cc-117">Les utilisateurs qui ont des ordinateurs clients Windows 2000 sur un domaine Windows 7 peuvent configurer un contrôleur de domaine Windows 2003/2008 dans le domaine et installer le service de support client de MSMQ Windows 2000 sur ce contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="a13cc-117">Users who have Windows 2000 Client machines on a Windows 7 domain can configure a Windows 2003/2008 domain controller in the domain and install the MSMQ Windows 2000 Client Support Service on this domain controller.</span></span>

### <a name="leveraging-feature-capabilities"></a><span data-ttu-id="a13cc-118">Exploitation des fonctionnalités de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="a13cc-118">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="a13cc-119">Les utilisateurs qui ont des ordinateurs clients Windows 2000 exécutant MSMQ doivent effectuer une mise à niveau vers une version plus récente de Windows afin de tirer parti de l’implémentation Active Directory du serveur MSMQ.</span><span class="sxs-lookup"><span data-stu-id="a13cc-119">Users who have Windows 2000 Client machines running MSMQ should upgrade to a higher Windows version in order to take advantage of the Active Directory-based implementation of the MSMQ Server.</span></span>

### <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="a13cc-120">Compatibilité, performances, fiabilité et test d’utilisabilité</span><span class="sxs-lookup"><span data-stu-id="a13cc-120">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="a13cc-121">Les utilisateurs qui ont des ordinateurs clients Windows 2000 exécutant MSMQ sur un domaine Windows 7 avec un ou plusieurs contrôleurs de domaine de niveau inférieure doivent vérifier que leurs applications sont opérationnelles sur ce domaine mixte.</span><span class="sxs-lookup"><span data-stu-id="a13cc-121">Users who have Windows 2000 Client machines running MSMQ on a Windows 7 domain with one or more down-level domain controllers should verify that their applications are functional on this mixed domain.</span></span>

 

 



