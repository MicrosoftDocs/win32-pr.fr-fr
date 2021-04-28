---
description: 'Méthode StartService de la classe Msvm_CollectionManagementService : arrête le service.'
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
ms.openlocfilehash: 18f58ae22cee06c439b6238df4c2a147405f7aca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112137"
---
# <a name="startservice-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="35e48-103">Méthode StartService de la \_ classe MSVM CollectionManagementService</span><span class="sxs-lookup"><span data-stu-id="35e48-103">StartService method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="35e48-104">arrête le service.</span><span class="sxs-lookup"><span data-stu-id="35e48-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="35e48-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35e48-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="35e48-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35e48-106">Parameters</span></span>

<span data-ttu-id="35e48-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="35e48-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="35e48-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="35e48-108">Return value</span></span>

<span data-ttu-id="35e48-109">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="35e48-109">Returns 0 if successful; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="35e48-110">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="35e48-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="35e48-111">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="35e48-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="35e48-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35e48-112">Requirements</span></span>



| <span data-ttu-id="35e48-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35e48-113">Requirement</span></span> | <span data-ttu-id="35e48-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="35e48-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35e48-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35e48-115">Minimum supported client</span></span><br/> | <span data-ttu-id="35e48-116">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35e48-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="35e48-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35e48-117">Minimum supported server</span></span><br/> | <span data-ttu-id="35e48-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="35e48-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="35e48-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="35e48-119">Namespace</span></span><br/>                | <span data-ttu-id="35e48-120">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="35e48-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="35e48-121">MOF</span><span class="sxs-lookup"><span data-stu-id="35e48-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35e48-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35e48-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="35e48-123">DLL</span><span class="sxs-lookup"><span data-stu-id="35e48-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35e48-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="35e48-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="35e48-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35e48-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35e48-126">**MSVM \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="35e48-126">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




