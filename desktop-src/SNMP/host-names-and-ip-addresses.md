---
title: Noms d’hôtes et adresses IP
description: Les réseaux TCP/IP requièrent que les noms d’hôte soient résolus en adresses IP avant que les informations d’adresse ne puissent être utilisées pour créer une connexion.
ms.assetid: f077e7d0-2e2c-4a2b-b5cd-1c7f43f7743b
keywords:
- Noms d’hôtes et adresses IP SNMP
- Noms d’hôtes, résolution SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426f711be9e1fda5dc936db6628cccc21093aa09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672586"
---
# <a name="host-names-and-ip-addresses"></a><span data-ttu-id="3287f-105">Noms d’hôtes et adresses IP</span><span class="sxs-lookup"><span data-stu-id="3287f-105">Host Names and IP Addresses</span></span>

<span data-ttu-id="3287f-106">Les réseaux TCP/IP requièrent que les noms d’hôte soient résolus en adresses IP avant que les informations d’adresse ne puissent être utilisées pour créer une connexion.</span><span class="sxs-lookup"><span data-stu-id="3287f-106">TCP/IP networks require host names to be resolved to IP addresses before the address information can be used to create a connection.</span></span> <span data-ttu-id="3287f-107">Les ordinateurs qui exécutent le système d’exploitation Windows utilisent un fichier d’hôte qui, à cet effet, mappe les noms d’hôte à des adresses IP.</span><span class="sxs-lookup"><span data-stu-id="3287f-107">Computers running on the Windows operating system use a host file that, for this purpose, maps host names to IP addresses.</span></span>

<span data-ttu-id="3287f-108">Le fichier hôte est un fichier texte qui répertorie les noms d’hôte et les adresses IP explicites.</span><span class="sxs-lookup"><span data-stu-id="3287f-108">The host file is a text file that lists explicit host names and IP addresses.</span></span> <span data-ttu-id="3287f-109">Le fichier hôte est automatiquement chargé en mémoire au démarrage et consulté lorsqu’un nom d’hôte requiert une résolution.</span><span class="sxs-lookup"><span data-stu-id="3287f-109">The host file is automatically loaded into memory on startup and consulted when a host name requires resolution.</span></span> <span data-ttu-id="3287f-110">Si le fichier hôte ne contient pas les informations de mappage requises pour résoudre un nom d’hôte spécifique en son adresse IP, une requête de résolution est effectuée sur un serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="3287f-110">If the host file does not contain the mapping information that is required to resolve a specific host name to its IP address, a resolution query is made to a DNS server.</span></span>

<span data-ttu-id="3287f-111">SNMP utilise le service WINS (Windows Internet Service de nommage) pour la résolution de noms d’hôte.</span><span class="sxs-lookup"><span data-stu-id="3287f-111">SNMP uses the Windows Internet Naming Service (WINS) for host name resolution.</span></span> <span data-ttu-id="3287f-112">WINS permet de mapper des noms NetBIOS, ou des noms de machine, à des adresses IP sur des réseaux TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="3287f-112">WINS makes it possible to map NetBIOS names, or machine names, to IP addresses on TCP/IP networks.</span></span> <span data-ttu-id="3287f-113">Si l’ordinateur ne peut pas accéder à un serveur WINS, le service SNMP utilise le fichier d’hôte pour résoudre les noms d’hôte en adresses IP.</span><span class="sxs-lookup"><span data-stu-id="3287f-113">If the computer cannot access a WINS server, the SNMP service uses the host file to resolve host names to IP addresses.</span></span>

<span data-ttu-id="3287f-114">Le service SNMP prend en charge l’utilisation des noms d’hôtes et des adresses IP.</span><span class="sxs-lookup"><span data-stu-id="3287f-114">The SNMP service supports the use of both host names and IP addresses.</span></span> <span data-ttu-id="3287f-115">Toutefois, lorsque vous avez le choix entre utiliser des noms d’hôte ou des adresses IP pour identifier les emplacements réseau, vos applications de gestion SNMP doivent utiliser des noms d’hôte.</span><span class="sxs-lookup"><span data-stu-id="3287f-115">However, when you have a choice between using host names or IP addresses to identify network locations, your SNMP management applications should use host names.</span></span> <span data-ttu-id="3287f-116">Si vous utilisez des noms d’hôte, ajoutez tous les mappages de nom d’hôte et d’adresse IP des systèmes participants au fichier hôte.</span><span class="sxs-lookup"><span data-stu-id="3287f-116">If you use host names, add all host name and IP address mappings of the participating systems to the host file.</span></span>

 

 




