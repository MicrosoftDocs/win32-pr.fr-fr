---
description: Authentification par carte à puce
ms.assetid: cb5c80ea-c15e-4f68-a94b-b458d69ff474
title: Authentification par carte à puce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241d323f4c5e982fee96f44002da316d5d645d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521112"
---
# <a name="smart-card-authentication"></a><span data-ttu-id="d65ee-103">Authentification par carte à puce</span><span class="sxs-lookup"><span data-stu-id="d65ee-103">Smart Card Authentication</span></span>

<span data-ttu-id="d65ee-104">Les composants de base du [*sous-système de carte à puce*](../secgloss/s-gly.md) sont basés sur les normes PC/SC (voir les spécifications à l’adresse [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ).</span><span class="sxs-lookup"><span data-stu-id="d65ee-104">The basic parts of the [*smart card subsystem*](../secgloss/s-gly.md) are based on PC/SC standards (see the specifications at [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/)).</span></span> <span data-ttu-id="d65ee-105">Ces éléments de base sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="d65ee-105">These basic parts include:</span></span>

-   <span data-ttu-id="d65ee-106">[*Gestionnaire de ressources*](../secgloss/r-gly.md) qui utilise une API Windows.</span><span class="sxs-lookup"><span data-stu-id="d65ee-106">A [*resource manager*](../secgloss/r-gly.md) that uses a Windows API.</span></span>
-   <span data-ttu-id="d65ee-107">[*Interface utilisateur*](../secgloss/u-gly.md) (IU) qui fonctionne avec le gestionnaire de ressources.</span><span class="sxs-lookup"><span data-stu-id="d65ee-107">A [*user interface*](../secgloss/u-gly.md) (UI) that works with the resource manager.</span></span>
-   <span data-ttu-id="d65ee-108">Plusieurs [*fournisseurs de services*](../secgloss/s-gly.md) de base qui fournissent un accès à des services spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d65ee-108">Several base [*service providers*](../secgloss/s-gly.md) that provide access to specific services.</span></span> <span data-ttu-id="d65ee-109">Contrairement à l’API Windows du gestionnaire de ressources, les fournisseurs de services utilisent un modèle d’interface COM pour fournir des services de [*carte à puce*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d65ee-109">In contrast to the resource manager's Windows API, service providers use a COM interface model to provide [*smart card*](../secgloss/s-gly.md) services.</span></span>

<span data-ttu-id="d65ee-110">L’illustration suivante montre les relations de ces parties dans l’architecture globale de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="d65ee-110">The following illustration shows the relationships of these parts in the overall smart card architecture.</span></span>

![architecture des cartes à puce](images/smartovr2a.png)

<span data-ttu-id="d65ee-112">Pour plus d’informations sur le fonctionnement du [*sous-système de carte à puce*](../secgloss/s-gly.md) avec d’autres services disponibles dans Microsoft Internet Security Framework, consultez [relation avec d’autres services](relation-to-other-services.md).</span><span class="sxs-lookup"><span data-stu-id="d65ee-112">For information about how the [*smart card subsystem*](../secgloss/s-gly.md) works with other services available in the Microsoft Internet Security Framework, see [Relation to Other Services](relation-to-other-services.md).</span></span>

<span data-ttu-id="d65ee-113">Pour plus d’informations sur l’authentification par carte à puce, consultez les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="d65ee-113">For information about smart card authentication, see the following topics.</span></span>



| <span data-ttu-id="d65ee-114">Rubriques</span><span class="sxs-lookup"><span data-stu-id="d65ee-114">Topics</span></span>                                                                      | <span data-ttu-id="d65ee-115">Contenu</span><span class="sxs-lookup"><span data-stu-id="d65ee-115">Contents</span></span>                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d65ee-116">Concepts de carte à puce</span><span class="sxs-lookup"><span data-stu-id="d65ee-116">Smart Card Concepts</span></span>](smart-card-concepts.md)<br/>                   | <span data-ttu-id="d65ee-117">Concepts de base et description de l’interaction entre les utilisateurs et les cartes à puce.</span><span class="sxs-lookup"><span data-stu-id="d65ee-117">Basic concepts and description of the interaction between users and smart cards.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="d65ee-118">Gestionnaire des ressources de carte à puce</span><span class="sxs-lookup"><span data-stu-id="d65ee-118">Smart Card Resource Manager</span></span>](smart-card-resource-manager.md)<br/>   | <span data-ttu-id="d65ee-119">Informations sur l’API Resource Manager, qui gère l’accès aux [*lecteurs*](../secgloss/r-gly.md) et aux [*cartes à puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d65ee-119">Information about the resource manager API, which manages the access to [*readers*](../secgloss/r-gly.md) and to [*smart cards*](../secgloss/s-gly.md).</span></span><br/> |
| [<span data-ttu-id="d65ee-120">Interface utilisateur de carte à puce</span><span class="sxs-lookup"><span data-stu-id="d65ee-120">Smart Card User Interface</span></span>](smart-card-user-interface.md)<br/>       | <span data-ttu-id="d65ee-121">Informations sur la [*boîte de dialogue commune de la carte à puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d65ee-121">Information about the [*smart card common dialog box*](../secgloss/s-gly.md).</span></span><br/>                                                                                   |
| [<span data-ttu-id="d65ee-122">Fournisseurs de services de carte à puce</span><span class="sxs-lookup"><span data-stu-id="d65ee-122">Smart Card Service Providers</span></span>](smart-card-service-providers.md)<br/> | <span data-ttu-id="d65ee-123">Informations sur les interfaces, les commandes et les wrappers qui fournissent des fonctionnalités de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="d65ee-123">Information about interfaces, commands, and wrappers that provide smart card capabilities.</span></span><br/>                                                                                                                                              |



 

<span data-ttu-id="d65ee-124">En outre, les développements des cartes à puce Microsoft sont disponibles à l’adresse [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx) .</span><span class="sxs-lookup"><span data-stu-id="d65ee-124">Additionally, current Microsoft smart card developments can be found at [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx).</span></span>

 

 
