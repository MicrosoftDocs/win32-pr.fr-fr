---
title: Pools de capteurs
description: 'Décrit trois pools de capteurs possibles : privé, privé et non assigné.'
ms.assetid: d7fd3c39-d719-4cfd-9af0-a87837f3f328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263275af5c7decff37ef70ad3a5396ec562562f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382192"
---
# <a name="sensor-pools"></a><span data-ttu-id="f72ac-103">Pools de capteurs</span><span class="sxs-lookup"><span data-stu-id="f72ac-103">Sensor Pools</span></span>

<span data-ttu-id="f72ac-104">Pour prendre en charge les scénarios d’authentification Windows et l’authentification définie par le fournisseur, le service de biométrie Windows organise les unités biométriques en trois pools de capteurs possibles :</span><span class="sxs-lookup"><span data-stu-id="f72ac-104">To support both Windows authentication scenarios and vendor defined authentication, the Windows Biometric service organizes biometric units into three possible sensor pools:</span></span>

-   <span data-ttu-id="f72ac-105">**Pool privé** collection d’unités biométriques allouées pour une utilisation exclusive par une application cliente.</span><span class="sxs-lookup"><span data-stu-id="f72ac-105">**Private pool** a collection of biometric units allocated for exclusive use by a client application.</span></span> <span data-ttu-id="f72ac-106">Les pools privés peuvent prendre en charge des scénarios d’authentification qui ne sont pas basés sur Windows, et ils permettent à une application d’accéder au matériel d’une unité biométrique de manière définie par un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f72ac-106">Private pools can support authentication scenarios that are not Windows-based, and they make it possible for an application to access the hardware of a biometric unit in a vendor-defined fashion.</span></span> <span data-ttu-id="f72ac-107">Il peut y avoir autant de pools de capteurs privés sur le système qu’il y a d’unités biométriques.</span><span class="sxs-lookup"><span data-stu-id="f72ac-107">There can be as many private sensor pools on the system as there are biometric units.</span></span>
-   <span data-ttu-id="f72ac-108">**Pool de capteurs système** collection d’unités biométriques partageables qui fournissent l’accès aux services d’authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="f72ac-108">**System sensor pool** a collection of sharable biometric units that provide access to Windows authentication services.</span></span> <span data-ttu-id="f72ac-109">Ce pool est utilisé par Winlogon, UAC et tout autre client qui associe un SID à un modèle biométrique spécifique.</span><span class="sxs-lookup"><span data-stu-id="f72ac-109">This pool is used by Winlogon, UAC, and any other client that associates a SID with a specific biometric template.</span></span> <span data-ttu-id="f72ac-110">Chaque fournisseur de services biométriques possède un pool de capteurs système.</span><span class="sxs-lookup"><span data-stu-id="f72ac-110">Each biometric service provider has one system sensor pool.</span></span>
-   <span data-ttu-id="f72ac-111">Le **pool non assigné** contient une collection (éventuellement vide) d’unités biométriques qui ne sont pas affectées au pool système ou au pool privé.</span><span class="sxs-lookup"><span data-stu-id="f72ac-111">**Unassigned pool** contains a (possibly empty) collection of biometric units that are not assigned to either the system pool or the private pool.</span></span>

<span data-ttu-id="f72ac-112">Les applications peuvent utiliser le pool de systèmes partagés ou créer un pool privé constitué d’unités biométriques supprimées du système ou de pools non attribués.</span><span class="sxs-lookup"><span data-stu-id="f72ac-112">Applications can use the shared system pool or they can create a private pool made up of biometric units removed from the system or unassigned pools.</span></span> <span data-ttu-id="f72ac-113">Quand une application libère son pool privé, les unités biométriques sont reconfigurées et retournées à leurs pools d’origine.</span><span class="sxs-lookup"><span data-stu-id="f72ac-113">When an application releases its private pool, the biometric units are reconfigured and returned to their original pools.</span></span> <span data-ttu-id="f72ac-114">Pour empêcher les attaques par déni de service, seuls les utilisateurs privilégiés sont autorisés à supprimer le dernier capteur du pool système.</span><span class="sxs-lookup"><span data-stu-id="f72ac-114">To prevent denial of service attacks, only privileged users are permitted to remove the last sensor from the system pool.</span></span> <span data-ttu-id="f72ac-115">Pour plus d'informations, consultez les rubriques ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="f72ac-115">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f72ac-116">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="f72ac-116">In this section</span></span>



| <span data-ttu-id="f72ac-117">Rubrique</span><span class="sxs-lookup"><span data-stu-id="f72ac-117">Topic</span></span>                                                       | <span data-ttu-id="f72ac-118">Description</span><span class="sxs-lookup"><span data-stu-id="f72ac-118">Description</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f72ac-119">Pool de capteurs privés</span><span class="sxs-lookup"><span data-stu-id="f72ac-119">Private Sensor Pool</span></span>](private-sensor-pool.md)<br/>   | <span data-ttu-id="f72ac-120">Collection d’unités biométriques réservée pour une utilisation exclusive par une application cliente.</span><span class="sxs-lookup"><span data-stu-id="f72ac-120">A collection of biometric units reserved for exclusive use by a client application.</span></span> <span data-ttu-id="f72ac-121">Les pools privés prennent en charge les méthodes d’authentification propriétaires et permettent à une application cliente d’accéder à une unité biométrique à l’aide de commandes de contrôle spécifiées par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f72ac-121">Private pools support proprietary authentication methods and enable a client application to access a biometric unit by using vendor-specified control commands.</span></span><br/> |
| [<span data-ttu-id="f72ac-122">Pool de capteurs système</span><span class="sxs-lookup"><span data-stu-id="f72ac-122">System Sensor Pool</span></span>](system-sensor-pool.md)<br/>     | <span data-ttu-id="f72ac-123">Collection d’unités biométriques partageables qui fournissent l’accès aux services d’authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="f72ac-123">A collection of sharable biometric units that provide access to Windows authentication services.</span></span> <span data-ttu-id="f72ac-124">Ce pool est utilisé par Winlogon, UAC et tout autre client qui associe un SID à un modèle biométrique spécifique.</span><span class="sxs-lookup"><span data-stu-id="f72ac-124">This pool is used by Winlogon, UAC, and any other client that associates a SID with a specific biometric template.</span></span><br/>                                 |
| [<span data-ttu-id="f72ac-125">Comportement du pool système</span><span class="sxs-lookup"><span data-stu-id="f72ac-125">System Pool Behavior</span></span>](system-pool-behavior.md)<br/> | <span data-ttu-id="f72ac-126">Discussion sur les actions effectuées par le pool système lorsque des notifications d’événements sont envoyées et lorsqu’aucune opération biométrique n’est en attente.</span><span class="sxs-lookup"><span data-stu-id="f72ac-126">Discussion about the actions taken by the system pool when event notices are sent and when no biometric operations are pending.</span></span><br/>                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="f72ac-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f72ac-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f72ac-128">À propos de l’API Windows Biometric Framework</span><span class="sxs-lookup"><span data-stu-id="f72ac-128">About the Windows Biometric Framework API</span></span>](./biometric-service-api-portal.md)
</dt> </dl>

 

