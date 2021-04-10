---
title: Activer et désactiver les rappels IGMP
description: Le gestionnaire de groupe de multidiffusion utilise deux rappels à IGMP pour coordonner les modifications de la propriété de l’interface de IGMP à un protocole de routage et d’un protocole de routage à IGMP.
ms.assetid: e4b2be85-6c67-4801-9905-eb1990d4bbb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aa58e9b65c67ac5946f5f5e54e611565e59d8c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842593"
---
# <a name="igmp-enable-and-disable-callbacks"></a><span data-ttu-id="79572-103">Activer et désactiver les rappels IGMP</span><span class="sxs-lookup"><span data-stu-id="79572-103">IGMP Enable and Disable Callbacks</span></span>

<span data-ttu-id="79572-104">Le gestionnaire de groupe de multidiffusion utilise deux rappels à IGMP pour coordonner les modifications de la propriété de l’interface de IGMP à un protocole de routage et d’un protocole de routage à IGMP.</span><span class="sxs-lookup"><span data-stu-id="79572-104">The multicast group manager uses two callbacks to IGMP to coordinate changes in interface ownership from IGMP to a routing protocol, and from a routing protocol to IGMP.</span></span> <span data-ttu-id="79572-105">Les rappels permettent à IGMP de coexister sur une interface avec un autre protocole de routage, tel que DVMRP.</span><span class="sxs-lookup"><span data-stu-id="79572-105">The callbacks enable IGMP to coexist on an interface with another routing protocol, such as DVMRP.</span></span>

<span data-ttu-id="79572-106">Une fois que la propriété d’une interface a changé, le gestionnaire de groupe de multidiffusion appelle d’abord le rappel de [**\_ \_ \_ rappel IGMP PMGM Disable**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) .</span><span class="sxs-lookup"><span data-stu-id="79572-106">After the ownership of an interface changes, the multicast group manager first invokes the [**PMGM\_DISABLE\_IGMP\_CALLBACK**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) callback.</span></span> <span data-ttu-id="79572-107">IGMP doit cesser d’ajouter et de supprimer des appartenances aux groupes sur l’interface spécifiée jusqu’à ce que le gestionnaire de groupe de multidiffusion appelle PMGM activer le rappel de [**\_ \_ \_ rappel IGMP**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) .</span><span class="sxs-lookup"><span data-stu-id="79572-107">IGMP must stop adding and deleting group memberships on the specified interface until the multicast group manager invokes the [**PMGM\_ENABLE\_IGMP\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) callback.</span></span>

<span data-ttu-id="79572-108">Le gestionnaire de groupe de multidiffusion appelle l’PMGM activer le rappel de [**\_ \_ \_ rappel IGMP**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) lorsque la modification de la propriété de l’interface est terminée.</span><span class="sxs-lookup"><span data-stu-id="79572-108">The multicast group manager invokes the [**PMGM\_ENABLE\_IGMP\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) callback after the change of interface ownership is complete.</span></span>

 

 