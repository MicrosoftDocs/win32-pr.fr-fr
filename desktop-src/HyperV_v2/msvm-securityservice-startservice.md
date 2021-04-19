---
description: démarre le service.
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
ms.openlocfilehash: bff2721b942b6bb145f2d57492f27d1cabb722bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535721"
---
# <a name="startservice-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="cda2b-103">Méthode StartService de la \_ classe MSVM securityservice</span><span class="sxs-lookup"><span data-stu-id="cda2b-103">StartService method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="cda2b-104">démarre le service.</span><span class="sxs-lookup"><span data-stu-id="cda2b-104">Starts the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="cda2b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cda2b-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="cda2b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cda2b-106">Parameters</span></span>

<span data-ttu-id="cda2b-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="cda2b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cda2b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cda2b-108">Return value</span></span>

<span data-ttu-id="cda2b-109">En cas de réussite, retourne 0 ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="cda2b-109">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="cda2b-110">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="cda2b-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cda2b-111">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="cda2b-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="cda2b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cda2b-112">Requirements</span></span>



| <span data-ttu-id="cda2b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cda2b-113">Requirement</span></span> | <span data-ttu-id="cda2b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="cda2b-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cda2b-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cda2b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cda2b-116">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cda2b-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cda2b-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cda2b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cda2b-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cda2b-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="cda2b-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cda2b-119">Namespace</span></span><br/>                | <span data-ttu-id="cda2b-120">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="cda2b-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cda2b-121">MOF</span><span class="sxs-lookup"><span data-stu-id="cda2b-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cda2b-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cda2b-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cda2b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="cda2b-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cda2b-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cda2b-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cda2b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cda2b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cda2b-126">**MSVM \_ securityservice**</span><span class="sxs-lookup"><span data-stu-id="cda2b-126">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




