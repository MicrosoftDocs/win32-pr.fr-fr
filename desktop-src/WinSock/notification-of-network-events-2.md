---
description: L’une des responsabilités les plus importantes d’un fournisseur de services de transport de données est celle qui consiste à fournir des indications au client lorsque certains événements réseau se sont produits.
ms.assetid: 7b60a775-ed20-4048-bd0b-9d43d090f82c
title: Notification des événements réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090d3adda7d34c0fe49eb14936bc01bf20878b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862549"
---
# <a name="notification-of-network-events"></a><span data-ttu-id="eb3db-103">Notification des événements réseau</span><span class="sxs-lookup"><span data-stu-id="eb3db-103">Notification of Network Events</span></span>

<span data-ttu-id="eb3db-104">L’une des responsabilités les plus importantes d’un fournisseur de services de transport de données est celle qui consiste à fournir des indications au client lorsque certains événements réseau se sont produits.</span><span class="sxs-lookup"><span data-stu-id="eb3db-104">One of the most important responsibilities of a data transport service provider is that of providing indications to the client when certain network events have occurred.</span></span> <span data-ttu-id="eb3db-105">La liste des événements réseau définis se compose des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="eb3db-105">The list of defined network events consists of the following:</span></span>

-   <span data-ttu-id="eb3db-106">**FD \_ Connexion : une** connexion à un hôte distant ou à une session de multidiffusion a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="eb3db-106">**FD\_CONNECT**— A connection to a remote host or to a multicast session has been completed.</span></span>
-   <span data-ttu-id="eb3db-107">**FD \_ ACCEPTER**: un hôte distant effectue une demande de connexion.</span><span class="sxs-lookup"><span data-stu-id="eb3db-107">**FD\_ACCEPT**— A remote host is making a connection request.</span></span>
-   <span data-ttu-id="eb3db-108">**FD \_ LECTURE**: les données réseau sont arrivées et peuvent être lues.</span><span class="sxs-lookup"><span data-stu-id="eb3db-108">**FD\_READ**— Network data has arrived which is available to be read.</span></span>
-   <span data-ttu-id="eb3db-109">**FD \_ WRITE**: l’espace est disponible dans les tampons du fournisseur de services afin que des données supplémentaires puissent désormais être envoyées.</span><span class="sxs-lookup"><span data-stu-id="eb3db-109">**FD\_WRITE**— Space has become available in the service provider's buffers so that additional data may now be sent.</span></span>
-   <span data-ttu-id="eb3db-110">**FD \_ OOB**: les données hors bande sont disponibles pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="eb3db-110">**FD\_OOB**— Out of band data is available to be read.</span></span>
-   <span data-ttu-id="eb3db-111">**FD \_ FERMER**: l’hôte distant a fermé la connexion.</span><span class="sxs-lookup"><span data-stu-id="eb3db-111">**FD\_CLOSE**— The remote host has closed down the connection.</span></span>
-   <span data-ttu-id="eb3db-112">**FD \_ QOS**: une modification a eu lieu dans les niveaux de QoS négocié.</span><span class="sxs-lookup"><span data-stu-id="eb3db-112">**FD\_QOS**— A change has occurred in negotiated QoS levels.</span></span>
-   <span data-ttu-id="eb3db-113">**FD \_ \_QoS de groupe**: réservé.</span><span class="sxs-lookup"><span data-stu-id="eb3db-113">**FD\_GROUP\_QOS**— Reserved.</span></span>
-   <span data-ttu-id="eb3db-114">**FD \_ \_ \_ Changement** de l’interface de routage : une interface locale qui doit être utilisée pour atteindre la destination spécifiée dans l' **interface de routage SIO modification de l' \_ \_ \_ IOCTL** a changé.</span><span class="sxs-lookup"><span data-stu-id="eb3db-114">**FD\_ROUTING\_INTERFACE\_CHANGE**— A local interface that should be used to reach the destination specified in **SIO\_ROUTING\_INTERFACE\_CHANGE IOCTL** has changed.</span></span>
-   <span data-ttu-id="eb3db-115">**FD \_ \_ \_ Modification** de la liste d’adresses : la liste des adresses locales auxquelles l’application peut se lier a changé.</span><span class="sxs-lookup"><span data-stu-id="eb3db-115">**FD\_ADDRESS\_LIST\_CHANGE**— The list of local addresses to which application can bind has changed.</span></span>

<span data-ttu-id="eb3db-116">Le jeu d’événements réseau énumérés ci-dessus est parfois appelé événements **FD \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="eb3db-116">The set of network events enumerated above is sometimes referred to as the **FD\_XXX** events.</span></span> <span data-ttu-id="eb3db-117">L’indication de l’occurrence d’un ou plusieurs de ces événements réseau peut être donnée de plusieurs façons, selon la manière dont le client demande la notification.</span><span class="sxs-lookup"><span data-stu-id="eb3db-117">Indication of the occurrence of one or more of such network events may be given in a number of ways depending on how the client requests notification.</span></span>

 

 



