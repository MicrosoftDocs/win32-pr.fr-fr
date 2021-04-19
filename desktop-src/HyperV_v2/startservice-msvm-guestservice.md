---
description: Met le service invité dans un état Démarré.
ms.assetid: 1DC6A5B3-0F91-4AC1-99D5-0E8CF5ED35A2
title: 'Msvm_GuestService :: StartService, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1a87bc9933bd7b3a54bd59169b0099e34eb04c52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523084"
---
# <a name="msvm_guestservicestartservice-method"></a><span data-ttu-id="e7437-103">MSVM \_ GuestService :: StartService, méthode</span><span class="sxs-lookup"><span data-stu-id="e7437-103">Msvm\_GuestService::StartService method</span></span>

<span data-ttu-id="e7437-104">Met le service invité dans un état Démarré.</span><span class="sxs-lookup"><span data-stu-id="e7437-104">Puts the guest service in a started state.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7437-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7437-105">Syntax</span></span>


```C++
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="e7437-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7437-106">Parameters</span></span>

<span data-ttu-id="e7437-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e7437-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7437-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7437-108">Return value</span></span>

<span data-ttu-id="e7437-109">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e7437-109">This method returns one of the following values.</span></span>



| <span data-ttu-id="e7437-110">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e7437-110">Return code/value</span></span>                                                                                                                                             | <span data-ttu-id="e7437-111">Description</span><span class="sxs-lookup"><span data-stu-id="e7437-111">Description</span></span>         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="e7437-112"><dt>**Terminé sans erreur**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e7437-112"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="e7437-113">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="e7437-113">Success.</span></span><br/> |
| <dl> <span data-ttu-id="e7437-114"><dt>**Non pris en charge**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e7437-114"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>           |                     |



 

## <a name="requirements"></a><span data-ttu-id="e7437-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7437-115">Requirements</span></span>



| <span data-ttu-id="e7437-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7437-116">Requirement</span></span> | <span data-ttu-id="e7437-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7437-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7437-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7437-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e7437-119">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7437-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e7437-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7437-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e7437-121">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7437-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e7437-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e7437-122">Namespace</span></span><br/>                | <span data-ttu-id="e7437-123">\\\\\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e7437-123">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="e7437-124">MOF</span><span class="sxs-lookup"><span data-stu-id="e7437-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7437-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7437-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7437-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e7437-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7437-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e7437-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e7437-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7437-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7437-129">**MSVM \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="e7437-129">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




