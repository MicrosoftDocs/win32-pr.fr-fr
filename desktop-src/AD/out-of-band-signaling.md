---
title: Signalisation hors bande
description: Les applications qui coopèrent qui partagent des données communes à l’aide de l’annuaire peuvent utiliser la signalisation hors bande pour éviter la distorsion de version et les mises à jour partielles.
ms.assetid: 82960273-5cda-44d2-bc17-d604f34f5a9b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc630bfdf3a2700ab187cd24bbfc5a52def1103
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028599"
---
# <a name="out-of-band-signaling"></a><span data-ttu-id="89799-103">Signalisation hors bande</span><span class="sxs-lookup"><span data-stu-id="89799-103">Out-of-Band Signaling</span></span>

<span data-ttu-id="89799-104">Les applications qui coopèrent qui partagent des données communes à l’aide de l’annuaire peuvent utiliser la signalisation hors bande pour éviter la distorsion de version et les mises à jour partielles.</span><span class="sxs-lookup"><span data-stu-id="89799-104">Cooperating applications that share common data using the directory can use out-of-band signaling to avoid both version skew and partial updates.</span></span> <span data-ttu-id="89799-105">En bref, les applications qui coopèrent utilisent un mécanisme distinct de la réplication d’annuaire pour s’informer mutuellement des modifications apportées aux données communes partagées.</span><span class="sxs-lookup"><span data-stu-id="89799-105">Put simply, the cooperating applications use a mechanism separate from directory replication to inform each other of changes in the shared common data.</span></span> <span data-ttu-id="89799-106">La signalisation hors bande est plus efficace lorsqu’elle est utilisée en association avec un mécanisme de contrôle de version, ce qui permet au partenaire de détecter la modification pour informer les partenaires distants de la version des données partagées à attendre.</span><span class="sxs-lookup"><span data-stu-id="89799-106">Out-of-band signaling is most effective when used in combination with a versioning mechanism—this allows the partner detecting the change to notify remote partners what version of the shared data to wait for.</span></span>

<span data-ttu-id="89799-107">En revenant à l’exemple RPC fourni dans la section « décalage de version » du [comportement de réplication dans Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md), le serveur RPC peut rappeler aux clients connectés pour les informer de la migration vers un nouveau serveur : «je vais le déplacer.</span><span class="sxs-lookup"><span data-stu-id="89799-107">Returning to the RPC example given in the "Version Skew" section of [Replication Behavior in Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md), the RPC server could call back into connected clients to inform them of the move to a new server: "I am going to move.</span></span> <span data-ttu-id="89799-108">Veillez à ce que la réplication vous apporte bientôt la nouvelle adresse. le client peut ainsi gérer la période de transition.</span><span class="sxs-lookup"><span data-stu-id="89799-108">Please stand by, replication will bring you the new address shortly" so that the client can handle the transition period.</span></span>

<span data-ttu-id="89799-109">Les applications qui requièrent des stratégies identiques pour être en mesure de communiquer entre elles peuvent utiliser la signalisation hors bande pour s’assurer qu’une nouvelle stratégie n’est pas utilisée tant que toutes les parties concernées ne l’ont pas reçue.</span><span class="sxs-lookup"><span data-stu-id="89799-109">Applications that require identical policies to be in force in order to communicate with each other can use out-of-band signaling to ensure that a new policy is not employed until all involved parties have received it.</span></span> <span data-ttu-id="89799-110">Par exemple, si la stratégie de sécurité du protocole Internet (IPsec) entre deux ordinateurs est modifiée, un agent sur la machine source peut contacter un agent sur l’ordinateur de destination pour négocier l’application de la stratégie modifiée, avec la machine source qui retarde l’application jusqu’à ce que l’ordinateur de destination ait reçu également la nouvelle stratégie.</span><span class="sxs-lookup"><span data-stu-id="89799-110">For example, if the Internet Protocol security (IPsec) policy between two machines is changed, an agent on the source machine could contact an agent on the destination machine to negotiate the application of the changed policy, with the source machine delaying application until the destination machine has received the new policy as well.</span></span>

 

 




