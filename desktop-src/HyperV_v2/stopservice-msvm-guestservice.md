---
description: Arrête le service invité.
ms.assetid: 67FFA46C-0B61-4845-A617-BA10F4D42CBC
title: 'Msvm_GuestService :: StopService, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6c396078e2bd623a768f391a645091679694f453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862362"
---
# <a name="msvm_guestservicestopservice-method"></a><span data-ttu-id="7c61a-103">MSVM \_ GuestService :: StopService, méthode</span><span class="sxs-lookup"><span data-stu-id="7c61a-103">Msvm\_GuestService::StopService method</span></span>

<span data-ttu-id="7c61a-104">Arrête le service invité.</span><span class="sxs-lookup"><span data-stu-id="7c61a-104">Stops the guest service.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c61a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c61a-105">Syntax</span></span>


```C++
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="7c61a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c61a-106">Parameters</span></span>

<span data-ttu-id="7c61a-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7c61a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c61a-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7c61a-108">Return value</span></span>

<span data-ttu-id="7c61a-109">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7c61a-109">This method returns one of the following values.</span></span>



| <span data-ttu-id="7c61a-110">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7c61a-110">Return code/value</span></span>                                                                                                                                             | <span data-ttu-id="7c61a-111">Description</span><span class="sxs-lookup"><span data-stu-id="7c61a-111">Description</span></span>         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="7c61a-112"><dt>**Terminé sans erreur**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7c61a-112"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="7c61a-113">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="7c61a-113">Success.</span></span><br/> |
| <dl> <span data-ttu-id="7c61a-114"><dt>**Non pris en charge**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7c61a-114"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>           |                     |



 

## <a name="requirements"></a><span data-ttu-id="7c61a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c61a-115">Requirements</span></span>



| <span data-ttu-id="7c61a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c61a-116">Requirement</span></span> | <span data-ttu-id="7c61a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c61a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c61a-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c61a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7c61a-119">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c61a-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="7c61a-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c61a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7c61a-121">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c61a-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7c61a-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7c61a-122">Namespace</span></span><br/>                | <span data-ttu-id="7c61a-123">\\\\\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="7c61a-123">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="7c61a-124">MOF</span><span class="sxs-lookup"><span data-stu-id="7c61a-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c61a-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c61a-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c61a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7c61a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c61a-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7c61a-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7c61a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c61a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c61a-129">**MSVM \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="7c61a-129">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




