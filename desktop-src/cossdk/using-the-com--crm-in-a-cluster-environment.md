---
description: Utilisation du CRM COM+ dans un environnement de cluster
ms.assetid: 753461c5-880c-4df0-b552-b962dc06524f
title: Utilisation du CRM COM+ dans un environnement de cluster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a05ff281748c35128349ef5d0d0f43d7beae86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317873"
---
# <a name="using-the-com-crm-in-a-cluster-environment"></a><span data-ttu-id="d1d35-103">Utilisation du CRM COM+ dans un environnement de cluster</span><span class="sxs-lookup"><span data-stu-id="d1d35-103">Using the COM+ CRM in a Cluster Environment</span></span>

<span data-ttu-id="d1d35-104">Lorsque vous développez des CRM CRM pour travailler dans des environnements de cluster, le principal facteur à prendre en compte est de savoir si un CRM spécifique détermine quel nœud du cluster sur lequel il est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="d1d35-104">When developing COM+ CRMs to work in cluster environments, the main factor to consider is whether a specific CRM cares which node of the cluster it is operating on.</span></span> <span data-ttu-id="d1d35-105">Par exemple, si la ressource gérée par le CRM est le système de fichiers de l’ordinateur ou le registre, toute modification est spécifique au nœud sur lequel l’application CRM Server est exécutée à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="d1d35-105">For example, if the resource managed by the CRM is the machine file system or registry, any changes are specific to the node that the CRM server application is running on at the time.</span></span> <span data-ttu-id="d1d35-106">Dans ce cas, le basculement de l’application CRM Server vers un autre nœud n’est pas souhaitable.</span><span class="sxs-lookup"><span data-stu-id="d1d35-106">In this case, failover of the CRM server application to another node would not be desirable.</span></span> <span data-ttu-id="d1d35-107">Dans un cas différent, où le CRM gère des ressources communes au cluster, le basculement de l’application CRM Server vers un autre nœud est utile.</span><span class="sxs-lookup"><span data-stu-id="d1d35-107">In a different case, where the CRM is managing some resource common to the cluster, failover of the CRM server application to another node is useful.</span></span>

<span data-ttu-id="d1d35-108">L’emplacement du répertoire par défaut pour les fichiers journaux CRM est le même que celui du fichier journal DTC.</span><span class="sxs-lookup"><span data-stu-id="d1d35-108">The default directory location for CRM log files is the same directory as the DTC log file.</span></span> <span data-ttu-id="d1d35-109">Sur les clusters, le fichier journal DTC est placé sur un disque partagé qui est basculé entre les nœuds du cluster.</span><span class="sxs-lookup"><span data-stu-id="d1d35-109">On clusters, the DTC log file is placed on a shared disk that is failed over between the nodes of the cluster.</span></span> <span data-ttu-id="d1d35-110">Cela signifie que le comportement par défaut pour les applications serveur CRM est le basculement entre les nœuds du cluster.</span><span class="sxs-lookup"><span data-stu-id="d1d35-110">This means that the default behavior for CRM server applications is to failover between nodes of the cluster.</span></span> <span data-ttu-id="d1d35-111">Par conséquent, si un CRM spécifique requiert un autre comportement qui consiste à ne pas basculer entre les nœuds, l’emplacement du fichier journal CRM pour cette application CRM Server particulière doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="d1d35-111">Therefore, if a specific CRM requires the alternative behavior of not failing over between nodes, the location of the CRM log file for that particular CRM server application should be changed.</span></span>

<span data-ttu-id="d1d35-112">En outre, si le basculement est requis pour l’application CRM, il doit être configuré en tant qu’application générique dans un groupe de clusters.</span><span class="sxs-lookup"><span data-stu-id="d1d35-112">In addition, if failover is required for the CRM application, it should be configured as a generic application in a cluster group.</span></span> <span data-ttu-id="d1d35-113">Sa dépendance doit être DTC.</span><span class="sxs-lookup"><span data-stu-id="d1d35-113">Its dependency should be DTC.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1d35-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d1d35-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1d35-115">Concepts de Gestionnaire des ressources de compensation COM+</span><span class="sxs-lookup"><span data-stu-id="d1d35-115">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



