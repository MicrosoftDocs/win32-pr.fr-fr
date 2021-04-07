---
title: Serveurs Active Directory et DNS dynamique
description: Les serveurs Active Directory publient leurs adresses afin que les clients puissent les trouver en connaissant uniquement le nom de domaine.
ms.assetid: b4928d53-2629-4ddb-bb43-ce7a187b41e2
ms.tgt_platform: multiple
keywords:
- Active Directory DNS dynamique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971987cb73b65e46b36eda4c713054ba2796e63b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671014"
---
# <a name="active-directory-servers-and-dynamic-dns"></a><span data-ttu-id="d0b23-104">Serveurs Active Directory et DNS dynamique</span><span class="sxs-lookup"><span data-stu-id="d0b23-104">Active Directory Servers and Dynamic DNS</span></span>

<span data-ttu-id="d0b23-105">Les serveurs Active Directory publient leurs adresses afin que les clients puissent les trouver en connaissant uniquement le nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="d0b23-105">The Active Directory servers publish their addresses such that clients can find them knowing only the domain name.</span></span> <span data-ttu-id="d0b23-106">Les serveurs Active Directory sont publiés à l’aide des enregistrements de ressource de service (RR SRV) dans DNS.</span><span class="sxs-lookup"><span data-stu-id="d0b23-106">Active Directory servers are published using the Service Resource Records (SRV RRs) in DNS.</span></span> <span data-ttu-id="d0b23-107">Le RR SRV est un enregistrement DNS utilisé pour mapper le nom d’un service à l’adresse d’un serveur qui offre le service.</span><span class="sxs-lookup"><span data-stu-id="d0b23-107">The SRV RR is a DNS record used to map the name of a service to the address of a server that offers the service.</span></span> <span data-ttu-id="d0b23-108">Le nom d’un enregistrement de ressource SRV se présente sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="d0b23-108">The name of a SRV RR is in this form:</span></span>


```C++
<service>.<protocol>.<domain>
```



<span data-ttu-id="d0b23-109">Les serveurs Active Directory offrent le service LDAP sur le protocole TCP afin que les noms publiés soient « LDAP. TCP <domain> ».</span><span class="sxs-lookup"><span data-stu-id="d0b23-109">Active Directory servers offer the LDAP service over the TCP protocol so that published names are "ldap.tcp.<domain>".</span></span> <span data-ttu-id="d0b23-110">Par conséquent, l’enregistrement de ressource SRV pour fabrikam.com est « ldap.tcp.fabrikam.com ».</span><span class="sxs-lookup"><span data-stu-id="d0b23-110">Thus, the SRV RR for fabrikam.com is "ldap.tcp.fabrikam.com".</span></span> <span data-ttu-id="d0b23-111">Des données supplémentaires sur le RR SRV indiquent la priorité et le poids du serveur, ce qui permet aux clients de choisir le serveur le mieux adapté à leurs besoins.</span><span class="sxs-lookup"><span data-stu-id="d0b23-111">Additional data about the SRV RR indicates the priority and weight for the server, enabling clients to choose the best server for their needs.</span></span>

<span data-ttu-id="d0b23-112">Lorsqu’un serveur Active Directory est installé, il utilise le DNS dynamique pour se publier lui-même.</span><span class="sxs-lookup"><span data-stu-id="d0b23-112">When an Active Directory server is installed, it uses Dynamic DNS to publish itself.</span></span> <span data-ttu-id="d0b23-113">Étant donné que les adresses TCP/IP sont sujettes à modification, les serveurs vérifient périodiquement leurs inscriptions pour s’assurer qu’elles sont correctes et les mettent à jour si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d0b23-113">Because TCP/IP addresses are subject to change, servers periodically verify their registrations to be sure they are correct, and update them if necessary.</span></span>

<span data-ttu-id="d0b23-114">Le DNS dynamique est un ajout récent à la norme DNS.</span><span class="sxs-lookup"><span data-stu-id="d0b23-114">Dynamic DNS is a recent addition to the DNS standard.</span></span> <span data-ttu-id="d0b23-115">Le DNS dynamique définit un protocole pour la mise à jour dynamique d’un serveur DNS avec de nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="d0b23-115">Dynamic DNS defines a protocol for dynamically updating a DNS server with new data.</span></span> <span data-ttu-id="d0b23-116">Avant le DNS dynamique, les administrateurs devaient configurer manuellement les enregistrements stockés par les serveurs DNS.</span><span class="sxs-lookup"><span data-stu-id="d0b23-116">Prior to Dynamic DNS, administrators were required to manually configure the records stored by DNS servers.</span></span>

 

 




