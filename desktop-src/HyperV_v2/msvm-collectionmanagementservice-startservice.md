---
description: arrête le service.
ms.assetid: 0f9a015d-b895-496a-a4c6-2737c0742746
title: Méthode StartService de la classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f76fa9e5069c2a9e19b83a8ab83136879c6657e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535638"
---
# <a name="startservice-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="24f76-103">Méthode StartService de la \_ classe MSVM CollectionManagementService</span><span class="sxs-lookup"><span data-stu-id="24f76-103">StartService method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="24f76-104">arrête le service.</span><span class="sxs-lookup"><span data-stu-id="24f76-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="24f76-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24f76-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="24f76-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24f76-106">Parameters</span></span>

<span data-ttu-id="24f76-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="24f76-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="24f76-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="24f76-108">Return value</span></span>

<span data-ttu-id="24f76-109">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="24f76-109">Returns 0 if successful; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="24f76-110">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="24f76-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="24f76-111">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="24f76-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="24f76-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24f76-112">Requirements</span></span>



| <span data-ttu-id="24f76-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24f76-113">Requirement</span></span> | <span data-ttu-id="24f76-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="24f76-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24f76-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24f76-115">Minimum supported client</span></span><br/> | <span data-ttu-id="24f76-116">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24f76-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="24f76-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24f76-117">Minimum supported server</span></span><br/> | <span data-ttu-id="24f76-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="24f76-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="24f76-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="24f76-119">Namespace</span></span><br/>                | <span data-ttu-id="24f76-120">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="24f76-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="24f76-121">MOF</span><span class="sxs-lookup"><span data-stu-id="24f76-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24f76-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="24f76-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="24f76-123">DLL</span><span class="sxs-lookup"><span data-stu-id="24f76-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24f76-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="24f76-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="24f76-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24f76-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24f76-126">**MSVM \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="24f76-126">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




