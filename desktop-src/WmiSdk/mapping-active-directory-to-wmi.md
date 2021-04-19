---
description: Le fournisseur de services d’annuaire met en miroir des classes et des instances de Active Directory dans l’espace de noms LDAP (Lightweight Directory Access Protocol) WMI.
ms.assetid: 0215b614-cb10-4195-837d-bf81d523c560
ms.tgt_platform: multiple
title: Mappage de Active Directory à WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e0162f722eb8a053270ac2a8e75eaed4f1cd405
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520610"
---
# <a name="mapping-active-directory-to-wmi"></a><span data-ttu-id="f4e87-103">Mappage de Active Directory à WMI</span><span class="sxs-lookup"><span data-stu-id="f4e87-103">Mapping Active Directory to WMI</span></span>

<span data-ttu-id="f4e87-104">Le fournisseur de services d’annuaire met en miroir des classes et des instances de Active Directory dans l’espace de noms LDAP (Lightweight Directory Access Protocol) WMI.</span><span class="sxs-lookup"><span data-stu-id="f4e87-104">The Directory Services Provider mirrors classes and instances from Active Directory into the WMI Lightweight Directory Access Protocol (LDAP) namespace.</span></span> <span data-ttu-id="f4e87-105">En raison des différences fondamentales dans les deux environnements, vous ne pouvez pas simplement renommer les classes et les instances de Active Directory et espérons qu’elles accèdent correctement à ces classes et instances dans WMI.</span><span class="sxs-lookup"><span data-stu-id="f4e87-105">Because of fundamental differences in the two environments, you cannot simply rename the Active Directory classes and instances and hope to properly access those classes and instances in WMI.</span></span> <span data-ttu-id="f4e87-106">Au lieu de cela, le fournisseur de services d’annuaire suit des règles d’affectation de noms pour conserver les relations qui existent entre les classes Active Directory et les instances.</span><span class="sxs-lookup"><span data-stu-id="f4e87-106">Instead, the Directory Services provider follows naming rules to preserve the relationships that exist between the Active Directory classes and instances.</span></span>

<span data-ttu-id="f4e87-107">Les rubriques suivantes fournissent des informations sur le mappage des classes et des instances de Active Directory :</span><span class="sxs-lookup"><span data-stu-id="f4e87-107">The following topics provide information about mapping Active Directory classes and instances:</span></span>

-   [<span data-ttu-id="f4e87-108">Mapper des classes Active Directory</span><span class="sxs-lookup"><span data-stu-id="f4e87-108">Mapping Active Directory Classes</span></span>](mapping-active-directory-classes.md)
-   [<span data-ttu-id="f4e87-109">Mappage d’instances Active Directory</span><span class="sxs-lookup"><span data-stu-id="f4e87-109">Mapping Active Directory Instances</span></span>](mapping-active-directory-instances.md)

> [!Note]  
> <span data-ttu-id="f4e87-110">Pour plus d’informations sur la prise en charge et l’installation de ce composant sur un système d’exploitation spécifique, consultez [disponibilité du système d’exploitation des composants WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="f4e87-110">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



