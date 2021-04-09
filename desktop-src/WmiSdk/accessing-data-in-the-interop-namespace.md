---
description: Les fournisseurs d’associations permettent aux clients Windows Management Instrumentation (WMI) de traverser et de récupérer des profils et des instances de classe associées à partir d’espaces de noms différents.
ms.assetid: 00c654d1-a5de-40c5-a190-99382949486a
ms.tgt_platform: multiple
title: Accès aux données dans l’espace de noms Interop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a217a7a44651b1a6c94476b53193eedac7f0d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952866"
---
# <a name="accessing-data-in-the-interop-namespace"></a><span data-ttu-id="76e20-103">Accès aux données dans l’espace de noms Interop</span><span class="sxs-lookup"><span data-stu-id="76e20-103">Accessing Data in the Interop Namespace</span></span>

<span data-ttu-id="76e20-104">Les fournisseurs d’associations permettent aux clients Windows Management Instrumentation (WMI) de traverser et de récupérer des profils et des instances de classe associées à partir d’espaces de noms différents.</span><span class="sxs-lookup"><span data-stu-id="76e20-104">Association providers enable Windows Management Instrumentation (WMI) clients to traverse and retrieve profiles and associated class instances from different namespaces.</span></span>

<span data-ttu-id="76e20-105">Les fournisseurs d’associations et les classes résident dans l' \\ \\ \\ espace de noms Interop racine.</span><span class="sxs-lookup"><span data-stu-id="76e20-105">Association providers and classes reside in the \\\\root\\interop namespace.</span></span> <span data-ttu-id="76e20-106">Pour plus d’informations, consultez parcours d’association d’un [espace de noms croisé](cross-namespace-association-traversal.md) et [écriture d’un fournisseur d’associations](writing-an-association-provider-for-interop.md).</span><span class="sxs-lookup"><span data-stu-id="76e20-106">For more information, see [Cross Namespace Association Traversal](cross-namespace-association-traversal.md) and [Writing an Association Provider](writing-an-association-provider-for-interop.md).</span></span>

<span data-ttu-id="76e20-107">Les fournisseurs d’associations exposent des profils standard, comme un profil d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="76e20-107">Association providers expose standard profiles, like a power profile.</span></span> <span data-ttu-id="76e20-108">Les exemples suivants utilisent le profil d’alimentation pour illustrer la découverte et l’accès aux données par le biais de l’espace de noms Interop.</span><span class="sxs-lookup"><span data-stu-id="76e20-108">The following examples use the power profile to illustrate how to discover and access data through the interop namespace.</span></span>

<span data-ttu-id="76e20-109">Windows PowerShell fournit un mécanisme simple pour parcourir l’Association appropriée, récupérer un profil d’appareil et appeler une méthode.</span><span class="sxs-lookup"><span data-stu-id="76e20-109">Windows PowerShell provides a simple mechanism to traverse through the appropriate association, retrieve a device profile, and call a method.</span></span>

## <a name="enumerating-profiles-in-the-rootinterop-namespace"></a><span data-ttu-id="76e20-110">Énumération des profils dans l’espace de noms root/Interop</span><span class="sxs-lookup"><span data-stu-id="76e20-110">Enumerating profiles in the root/interop namespace</span></span>

<span data-ttu-id="76e20-111">La commande Windows PowerShell suivante énumère les profils pris en charge par la force de gestion distribuée ([DMTF](https://www.dmtf.org/standards/wsman)) sur un ordinateur Windows 7 :</span><span class="sxs-lookup"><span data-stu-id="76e20-111">The following Windows PowerShell command enumerates the Distributed Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman))-supported profiles on a Windows 7 computer:</span></span>


```PowerShell
Get-WmiObject CIM_RegisteredProfile  -namespace root\interop
```



## <a name="retrieving-instances-of-a-specific-device-profile"></a><span data-ttu-id="76e20-112">Récupération des instances d’un profil d’appareil spécifique</span><span class="sxs-lookup"><span data-stu-id="76e20-112">Retrieving instances of a specific device profile</span></span>

<span data-ttu-id="76e20-113">La commande Windows PowerShell suivante retourne toutes les instances d’un profil spécifié par le biais de [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="76e20-113">The following Windows PowerShell command returns all instances of a specified profile through [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)):</span></span>


```PowerShell
Get-WmiObject -namespace root\interop -query "Associators of {CIM_RegisteredProfile.InstanceID='Power Supply'}"
```



## <a name="assigning-the-power-profile-to-a-variable"></a><span data-ttu-id="76e20-114">Affectation du profil d’alimentation à une variable</span><span class="sxs-lookup"><span data-stu-id="76e20-114">Assigning the power profile to a variable</span></span>

<span data-ttu-id="76e20-115">La commande Windows PowerShell suivante affecte l’instance de profil d’alimentation à une variable :</span><span class="sxs-lookup"><span data-stu-id="76e20-115">The following Windows PowerShell command assigns the power profile instance to a variable:</span></span>


```PowerShell
$pplan = Get-WmiObject -query "Select * from Win32_PowerPlan" -Namespace root\cimv2\power
```



## <a name="enumerating-the-power-plans-on-a-computer"></a><span data-ttu-id="76e20-116">Énumération des modes de gestion de l’alimentation d’un ordinateur</span><span class="sxs-lookup"><span data-stu-id="76e20-116">Enumerating the power plans on a computer</span></span>

<span data-ttu-id="76e20-117">La commande Windows PowerShell suivante énumère les plans de profil d’alimentation disponibles :</span><span class="sxs-lookup"><span data-stu-id="76e20-117">The following Windows PowerShell command enumerates the available power profile plans:</span></span>


```PowerShell
$pplan
```



## <a name="calling-a-method"></a><span data-ttu-id="76e20-118">Appel d'une méthode</span><span class="sxs-lookup"><span data-stu-id="76e20-118">Calling a method</span></span>

<span data-ttu-id="76e20-119">La commande Windows PowerShell suivante appelle la méthode [**Activate**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) pour le mode de gestion de l’alimentation :</span><span class="sxs-lookup"><span data-stu-id="76e20-119">The following Windows PowerShell command calls the [**Activate**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) method for the power plan:</span></span>


```PowerShell
$pplan[2].Activate()
```



## <a name="related-topics"></a><span data-ttu-id="76e20-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="76e20-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76e20-121">Traversée des associations entre espaces de noms</span><span class="sxs-lookup"><span data-stu-id="76e20-121">Cross Namespace Association Traversal</span></span>](cross-namespace-association-traversal.md)
</dt> <dt>

[<span data-ttu-id="76e20-122">Écriture d’un fournisseur d’association</span><span class="sxs-lookup"><span data-stu-id="76e20-122">Writing an Association Provider</span></span>](writing-an-association-provider-for-interop.md)
</dt> <dt>

<span data-ttu-id="76e20-123">[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="76e20-123">[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="76e20-124">[**\_PowerPlan Win32**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="76e20-124">[**Win32\_PowerPlan**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))</span></span>
</dt> </dl>

 

 
