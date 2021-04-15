---
title: EnableDCOM
description: Contrôle l’activation globale et les stratégies d’appel de l’ordinateur. Seuls les administrateurs et le système ont un accès complet à cette partie du Registre. Tous les autres utilisateurs disposent d’un accès en lecture seule.
ms.assetid: 8533270d-f1b0-42b9-a50d-b05a0dfeee22
keywords:
- Valeur de Registre EnableDCOM COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42cc95b24522e87e4b64f6feefc5c6c56ad5341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379786"
---
# <a name="enabledcom"></a><span data-ttu-id="54798-106">EnableDCOM</span><span class="sxs-lookup"><span data-stu-id="54798-106">EnableDCOM</span></span>

<span data-ttu-id="54798-107">Contrôle l’activation globale et les stratégies d’appel de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="54798-107">Controls the global activation and call policies of the machine.</span></span> <span data-ttu-id="54798-108">Seuls les administrateurs et le système ont un accès complet à cette partie du Registre.</span><span class="sxs-lookup"><span data-stu-id="54798-108">Only administrators and the system have full access to this portion of the registry.</span></span> <span data-ttu-id="54798-109">Tous les autres utilisateurs disposent d’un accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="54798-109">All other users have read-only access.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="54798-110">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="54798-110">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   EnableDCOM = value
```

## <a name="remarks"></a><span data-ttu-id="54798-111">Notes</span><span class="sxs-lookup"><span data-stu-id="54798-111">Remarks</span></span>

<span data-ttu-id="54798-112">Il s’agit d’une valeur de **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="54798-112">This is a **REG\_SZ** value.</span></span>



| <span data-ttu-id="54798-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="54798-113">Value</span></span>    | <span data-ttu-id="54798-114">Description</span><span class="sxs-lookup"><span data-stu-id="54798-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54798-115">N (ou n)</span><span class="sxs-lookup"><span data-stu-id="54798-115">N (or n)</span></span> | <span data-ttu-id="54798-116">Aucun client distant ne peut lancer des serveurs ou se connecter à des objets sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="54798-116">No remote clients may launch servers or connect to objects on this computer.</span></span> <span data-ttu-id="54798-117">Les clients locaux ne peuvent pas accéder aux serveurs DCOM distants ; tout le trafic DCOM est bloqué.</span><span class="sxs-lookup"><span data-stu-id="54798-117">Local clients cannot access remote DCOM servers; all DCOM traffic is blocked.</span></span> <span data-ttu-id="54798-118">Le lancement local de code de classe et la connexion aux objets sont autorisés par classe en fonction de la valeur et des autorisations d’accès de la valeur de Registre [**LaunchPermission**](launchpermission.md) de la classe et de la valeur de Registre [**DefaultLaunchPermission**](defaultlaunchpermission.md) globale.</span><span class="sxs-lookup"><span data-stu-id="54798-118">Local launching of class code and connecting to objects are allowed on a per-class basis according to the value and access permissions of the class's [**LaunchPermission**](launchpermission.md) registry value and the global [**DefaultLaunchPermission**](defaultlaunchpermission.md) registry value.</span></span> |
| <span data-ttu-id="54798-119">Y (ou y)</span><span class="sxs-lookup"><span data-stu-id="54798-119">Y (or y)</span></span> | <span data-ttu-id="54798-120">Le lancement de serveurs et la connexion aux objets par des clients distants sont autorisés par classe en fonction de la valeur et des autorisations d’accès de la valeur de Registre [**LaunchPermission**](launchpermission.md) de la classe et de la valeur de Registre [**DefaultLaunchPermission**](defaultlaunchpermission.md) globale.</span><span class="sxs-lookup"><span data-stu-id="54798-120">Launching of servers and connecting to objects by remote clients is allowed on a per-class basis according to the value and access permissions of the class's [**LaunchPermission**](launchpermission.md) registry value and the global [**DefaultLaunchPermission**](defaultlaunchpermission.md) registry value.</span></span>                                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="54798-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="54798-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54798-122">**DefaultLaunchPermission**</span><span class="sxs-lookup"><span data-stu-id="54798-122">**DefaultLaunchPermission**</span></span>](defaultlaunchpermission.md)
</dt> <dt>

[<span data-ttu-id="54798-123">**LaunchPermission**</span><span class="sxs-lookup"><span data-stu-id="54798-123">**LaunchPermission**</span></span>](launchpermission.md)
</dt> <dt>

[<span data-ttu-id="54798-124">Sécurité dans COM</span><span class="sxs-lookup"><span data-stu-id="54798-124">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




