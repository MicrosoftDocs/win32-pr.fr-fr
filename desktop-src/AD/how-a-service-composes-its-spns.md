---
title: Comment un service compose ses SPN
description: Un service peut utiliser deux fonctions pour composer ses SPN DsGetSpn est une fonction à usage général pour composer des SPN et DsServerRegisterSpn est une fonction spécialisée pour composer et inscrire des SPN simples pour un service basé sur l’hôte.
ms.assetid: 8710409a-67b1-45e5-9cd7-5125443ab921
ms.tgt_platform: multiple
keywords:
- nom de principal du service AD, comment un service est composé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5611527cc3c240eebc195058ce39daab71aeef23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839313"
---
# <a name="how-a-service-composes-its-spns"></a><span data-ttu-id="5e183-104">Comment un service compose ses SPN</span><span class="sxs-lookup"><span data-stu-id="5e183-104">How a Service Composes its SPNs</span></span>

<span data-ttu-id="5e183-105">Un service peut utiliser deux fonctions pour composer ses SPN : [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) est une fonction à usage général pour composer des SPN et [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) est une fonction spécialisée pour composer et inscrire des SPN simples pour un service basé sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="5e183-105">A service can use two functions to compose its SPNs: [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) is a general-purpose function for composing SPNs and [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) is a specialized function for composing and registering simple SPNs for a host-based service.</span></span>

<span data-ttu-id="5e183-106">Un programme d’installation de service utilise généralement la fonction [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) pour composer des SPN, qu’il enregistre ensuite sur le compte d’ouverture de session du service à l’aide de la fonction [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) .</span><span class="sxs-lookup"><span data-stu-id="5e183-106">A service installer typically uses the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) function to compose SPNs, which it then registers on the service's logon account using the [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) function.</span></span> <span data-ttu-id="5e183-107">Le **DsGetSpn** peut exécuter les fonctions suivantes.</span><span class="sxs-lookup"><span data-stu-id="5e183-107">The **DsGetSpn** can perform the following functions.</span></span>

-   <span data-ttu-id="5e183-108">Créez un SPN simple avec le <service class> / <host> format «» pour un service basé sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="5e183-108">Create a simple SPN with the "<service class>/<host>" format for a host-based service.</span></span>
-   <span data-ttu-id="5e183-109">Créez un nom de principal du service (SPN) complexe qui comprend le &lt; composant « nom du service &gt; » utilisé par les services réplicables ou le &lt; composant « port &gt; » qui distingue plusieurs instances d’un service sur un seul hôte.</span><span class="sxs-lookup"><span data-stu-id="5e183-109">Create a complex SPN that includes the "&lt;service name&gt;" component used by replicable services or the "&lt;port&gt;" component that distinguishes multiple instances of a service on a single host.</span></span>
-   <span data-ttu-id="5e183-110">Créez un SPN unique avec le &lt; composant « hôte &gt; » défini sur le nom d’un ordinateur hôte spécifié ou sur le nom de l’ordinateur local par défaut.</span><span class="sxs-lookup"><span data-stu-id="5e183-110">Create a single SPN with the "&lt;host&gt;" component set to either the name of a specified host or the name of the local computer by default.</span></span>
-   <span data-ttu-id="5e183-111">Créez un tableau de noms de principal du service pour plusieurs instances de service qui s’exécuteront sur plusieurs hôtes dans l’ensemble de la forêt.</span><span class="sxs-lookup"><span data-stu-id="5e183-111">Create an array of SPNs for multiple service instances that will run on multiple hosts throughout the forest.</span></span> <span data-ttu-id="5e183-112">Chaque SPN spécifie le nom de l’hôte pour une instance de service.</span><span class="sxs-lookup"><span data-stu-id="5e183-112">Each SPN specifies the name of the host for a service instance.</span></span>
-   <span data-ttu-id="5e183-113">Créez un tableau de noms de principal du service pour plusieurs instances de service qui s’exécuteront sur le même hôte.</span><span class="sxs-lookup"><span data-stu-id="5e183-113">Create an array of SPNs for multiple service instances that will run on the same host.</span></span> <span data-ttu-id="5e183-114">Chaque SPN spécifie le nom de l’hôte et un numéro de port pour une instance de service.</span><span class="sxs-lookup"><span data-stu-id="5e183-114">Each SPN specifies the name of the host and a port number for a service instance.</span></span>

<span data-ttu-id="5e183-115">Le tableau des noms retournés par [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) doit être libéré en appelant la fonction [**DsFreeSpnArray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya) .</span><span class="sxs-lookup"><span data-stu-id="5e183-115">The array of names returned by [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) must be freed by calling the [**DsFreeSpnArray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya) function.</span></span>

<span data-ttu-id="5e183-116">N’oubliez pas que les fonctions [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna), [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)et [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) ne vérifient pas que les noms principaux de service sont uniques.</span><span class="sxs-lookup"><span data-stu-id="5e183-116">Be aware that the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna), [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna), and [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) functions do not verify that SPNs are unique.</span></span> <span data-ttu-id="5e183-117">Étant donné que l’authentification mutuelle échoue si un client présente un nom de principal du service qui n’est pas unique, vérifiez l’unicité avant d’inscrire un SPN.</span><span class="sxs-lookup"><span data-stu-id="5e183-117">Because mutual authentication fails if a client presents an SPN that is not unique, verify uniqueness before registering an SPN.</span></span> <span data-ttu-id="5e183-118">Pour ce faire, recherchez dans le catalogue global (GC) les attributs **servicePrincipalName** qui correspondent à votre SPN.</span><span class="sxs-lookup"><span data-stu-id="5e183-118">To do this, search the global catalog (GC) for **servicePrincipalName** attributes that match your SPN.</span></span> <span data-ttu-id="5e183-119">Pour plus d’informations sur la recherche dans le GC, consultez [recherche dans le catalogue global](searching-global-catalog-contents.md).</span><span class="sxs-lookup"><span data-stu-id="5e183-119">For more information about searching the GC, see [Searching the Global Catalog](searching-global-catalog-contents.md).</span></span>

 

 




