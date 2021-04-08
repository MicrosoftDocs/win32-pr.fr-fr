---
title: Localisation d’un serveur hôte de partition d’annuaire d’applications
description: Cette rubrique explique comment localiser un serveur hôte de partition de l’annuaire d’applications.
ms.assetid: 636e8bc2-136c-42be-aa64-1b059dedf775
ms.tgt_platform: multiple
keywords:
- Recherche d’un serveur hôte de partition d’annuaire d’applications AD
- Partitions de l’annuaire d’applications Active Directory, localisation d’un serveur hôte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c9e8f80ccf4b1549af9a76e7b588685d38c297
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671270"
---
# <a name="locating-an-application-directory-partition-host-server"></a><span data-ttu-id="100f9-105">Localisation d’un serveur hôte de partition d’annuaire d’applications</span><span class="sxs-lookup"><span data-stu-id="100f9-105">Locating an Application Directory Partition Host Server</span></span>

<span data-ttu-id="100f9-106">Le service Netlogon inscrit la liste suivante d’enregistrements SRV pour une partition de l’annuaire d’applications :</span><span class="sxs-lookup"><span data-stu-id="100f9-106">The NetLogon service registers the following list of SRV records for an application directory partition:</span></span>

-   <span data-ttu-id="100f9-107">\_LDAP. \_ protocoles.<partition name></span><span class="sxs-lookup"><span data-stu-id="100f9-107">\_ldap.\_tcp.<partition name></span></span>
-   <span data-ttu-id="100f9-108">\_LDAP. \_ TCP. <site name> . \_ sites.<partition name></span><span class="sxs-lookup"><span data-stu-id="100f9-108">\_ldap.\_tcp.<site name>.\_sites.<partition name></span></span>

<span data-ttu-id="100f9-109">Pour localiser un contrôleur de domaine qui héberge un réplica d’une partition d’annuaire d’applications spécifiée, appelez la fonction [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) avec le paramètre *domainname* défini sur le nom DNS de la partition de l’annuaire d’applications et l’indicateur **DS \_ uniquement \_ LDAP \_ requis** défini dans le paramètre *Flags* .</span><span class="sxs-lookup"><span data-stu-id="100f9-109">To locate a domain controller that hosts a replica of a specified application directory partition, call the [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) function with the *DomainName* parameter set to the DNS name of the application directory partition and the **DS\_ONLY\_LDAP\_NEEDED** flag set in the *Flags* parameter.</span></span> <span data-ttu-id="100f9-110">Pour plus d’informations et pour obtenir un exemple de code qui montre, à l’aide de la fonction **DsGetDcName** , comment localiser un contrôleur de domaine qui héberge un réplica d’une partition d’annuaire d’applications, consultez l' [exemple de code pour localiser un serveur hôte de partition d’annuaire d’applications](example-code-for-locating-an-application-directory-partition-host-server.md).</span><span class="sxs-lookup"><span data-stu-id="100f9-110">For more information and a code example that shows, using the **DsGetDcName** function, how to locate a domain controller that hosts a replica of an application directory partition, see [Example Code for Locating an Application Directory Partition Host Server](example-code-for-locating-an-application-directory-partition-host-server.md).</span></span>

 

 




