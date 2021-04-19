---
description: arrête le service.
ms.assetid: cf0dde8d-b6cf-4a52-905f-c686ac41e314
title: Méthode StopService de la classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f815b400101bbddf019026675c69421bcc2c6598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514577"
---
# <a name="stopservice-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="91c9a-103">Méthode StopService de la \_ classe MSVM VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="91c9a-103">StopService method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="91c9a-104">arrête le service.</span><span class="sxs-lookup"><span data-stu-id="91c9a-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="91c9a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91c9a-105">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="91c9a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91c9a-106">Parameters</span></span>

<span data-ttu-id="91c9a-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="91c9a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="91c9a-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91c9a-108">Return value</span></span>

<span data-ttu-id="91c9a-109">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="91c9a-109">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="91c9a-110">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="91c9a-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="91c9a-111">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="91c9a-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="91c9a-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91c9a-112">Requirements</span></span>



| <span data-ttu-id="91c9a-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91c9a-113">Requirement</span></span> | <span data-ttu-id="91c9a-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="91c9a-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91c9a-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91c9a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="91c9a-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="91c9a-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="91c9a-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91c9a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="91c9a-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="91c9a-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="91c9a-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="91c9a-119">Namespace</span></span><br/>                | <span data-ttu-id="91c9a-120">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="91c9a-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="91c9a-121">MOF</span><span class="sxs-lookup"><span data-stu-id="91c9a-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91c9a-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="91c9a-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="91c9a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="91c9a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91c9a-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="91c9a-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="91c9a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91c9a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91c9a-126">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="91c9a-126">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




