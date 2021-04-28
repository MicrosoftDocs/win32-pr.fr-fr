---
description: Méthode StartService de la classe Msvm_SecurityService-démarre le service.
ms.assetid: 59918c15-7216-4cf7-9215-b27532febc72
title: Méthode StartService de la classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31e16eea84cf61ace11c241b6409a5810f74b8f1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111397"
---
# <a name="startservice-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="001d3-103">Méthode StartService de la \_ classe MSVM securityservice</span><span class="sxs-lookup"><span data-stu-id="001d3-103">StartService method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="001d3-104">démarre le service.</span><span class="sxs-lookup"><span data-stu-id="001d3-104">Starts the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="001d3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="001d3-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="001d3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="001d3-106">Parameters</span></span>

<span data-ttu-id="001d3-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="001d3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="001d3-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="001d3-108">Return value</span></span>

<span data-ttu-id="001d3-109">En cas de réussite, retourne 0 ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="001d3-109">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="001d3-110">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="001d3-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="001d3-111">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="001d3-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="001d3-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="001d3-112">Requirements</span></span>



| <span data-ttu-id="001d3-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="001d3-113">Requirement</span></span> | <span data-ttu-id="001d3-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="001d3-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="001d3-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="001d3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="001d3-116">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="001d3-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="001d3-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="001d3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="001d3-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="001d3-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="001d3-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="001d3-119">Namespace</span></span><br/>                | <span data-ttu-id="001d3-120">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="001d3-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="001d3-121">MOF</span><span class="sxs-lookup"><span data-stu-id="001d3-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="001d3-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="001d3-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="001d3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="001d3-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="001d3-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="001d3-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="001d3-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="001d3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="001d3-126">**MSVM \_ securityservice**</span><span class="sxs-lookup"><span data-stu-id="001d3-126">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




