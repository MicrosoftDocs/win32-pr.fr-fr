---
title: MachineLaunchRestriction
description: Définit la stratégie de restriction à l’ensemble de l’ordinateur pour le lancement et l’activation de composants.
ms.assetid: 274e3d08-1f38-4179-b7e7-b218d6e184ee
keywords:
- Valeur de Registre MachineLaunchRestriction COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14dfcfe5535871c6b5b0fe310c94b920c522f05a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197278"
---
# <a name="machinelaunchrestriction"></a><span data-ttu-id="dfca3-104">MachineLaunchRestriction</span><span class="sxs-lookup"><span data-stu-id="dfca3-104">MachineLaunchRestriction</span></span>

<span data-ttu-id="dfca3-105">Définit la stratégie de restriction à l’ensemble de l’ordinateur pour le lancement et l’activation de composants.</span><span class="sxs-lookup"><span data-stu-id="dfca3-105">Sets the computer-wide restriction policy for component launch and activation.</span></span>

> [!Caution]  
> <span data-ttu-id="dfca3-106">La modification de cette valeur affecte toutes les applications serveur COM et peut les empêcher de fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="dfca3-106">Changing this value will affect all COM server applications, and might prevent them from working properly.</span></span> <span data-ttu-id="dfca3-107">Si des applications serveur COM présentent des restrictions moins strictes que les restrictions à l’niveau de l’ordinateur, la réduction des restrictions de l’ordinateur peut exposer ces applications à un accès indésirable.</span><span class="sxs-lookup"><span data-stu-id="dfca3-107">If there are COM server applications that have restrictions that are less stringent than the computer-wide restrictions, reducing the computer-wide restrictions may expose these applications to unwanted access.</span></span> <span data-ttu-id="dfca3-108">À l’inverse, si vous augmentez les restrictions au niveau de l’ordinateur, certaines applications serveur COM peuvent ne plus être accessibles en appelant des applications.</span><span class="sxs-lookup"><span data-stu-id="dfca3-108">Conversely, if you increase the computer-wide restrictions, some COM server applications might no longer be accessible by calling applications.</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="dfca3-109">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="dfca3-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineLaunchRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a><span data-ttu-id="dfca3-110">Notes</span><span class="sxs-lookup"><span data-stu-id="dfca3-110">Remarks</span></span>

<span data-ttu-id="dfca3-111">Il s’agit d’une valeur **\_ binaire de Reg** .</span><span class="sxs-lookup"><span data-stu-id="dfca3-111">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="dfca3-112">Les principaux qui ne reçoivent pas d’autorisations ici ne peuvent pas les obtenir, même si les autorisations sont accordées par la valeur de Registre [DefaultAccessPermission](defaultaccesspermission.md) ou par la fonction [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="dfca3-112">Principals not given permissions here cannot obtain them even if the permissions are granted by the [DefaultAccessPermission](defaultaccesspermission.md) registry value or by the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) function.</span></span>

<span data-ttu-id="dfca3-113">Par défaut, les administrateurs peuvent obtenir des autorisations d’exécution et d’activation locales et à distance, et les membres du groupe tout le monde peuvent obtenir des autorisations d’activation locale et de lancement.</span><span class="sxs-lookup"><span data-stu-id="dfca3-113">By default, administrators may obtain local and remote launch and activation permissions, and members of the Everyone group may obtain local activation and launch permissions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dfca3-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dfca3-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfca3-115">Définition de la sécurité pour les applications COM</span><span class="sxs-lookup"><span data-stu-id="dfca3-115">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




