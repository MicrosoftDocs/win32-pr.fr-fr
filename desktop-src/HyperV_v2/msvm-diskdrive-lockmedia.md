---
description: Verrouille ou déverrouille le média.
ms.assetid: 805efb2d-71a7-4c74-821f-942644928ff9
title: Méthode LockMedia de la classe Msvm_DiskDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7ddc082ca6ceb7141eaa42bdfddf7a97897a9240
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106522505"
---
# <a name="lockmedia-method-of-the-msvm_diskdrive-class"></a><span data-ttu-id="87bf1-103">Méthode LockMedia de la \_ classe DiskDrive MSVM</span><span class="sxs-lookup"><span data-stu-id="87bf1-103">LockMedia method of the Msvm\_DiskDrive class</span></span>

<span data-ttu-id="87bf1-104">Verrouille ou déverrouille le média.</span><span class="sxs-lookup"><span data-stu-id="87bf1-104">Locks or unlocks the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="87bf1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87bf1-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="87bf1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87bf1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87bf1-107">*Verrou* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="87bf1-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87bf1-108">**true** pour verrouiller le média ; **false** pour libérer le média.</span><span class="sxs-lookup"><span data-stu-id="87bf1-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87bf1-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="87bf1-109">Return value</span></span>

<span data-ttu-id="87bf1-110">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="87bf1-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="87bf1-111">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="87bf1-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="87bf1-112">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="87bf1-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="87bf1-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87bf1-113">Requirements</span></span>



| <span data-ttu-id="87bf1-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87bf1-114">Requirement</span></span> | <span data-ttu-id="87bf1-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="87bf1-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87bf1-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87bf1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="87bf1-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="87bf1-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="87bf1-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87bf1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="87bf1-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="87bf1-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="87bf1-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="87bf1-120">Namespace</span></span><br/>                | <span data-ttu-id="87bf1-121">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="87bf1-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="87bf1-122">MOF</span><span class="sxs-lookup"><span data-stu-id="87bf1-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87bf1-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87bf1-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="87bf1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="87bf1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87bf1-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="87bf1-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="87bf1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87bf1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87bf1-127">**MSVM \_ DiskDrive**</span><span class="sxs-lookup"><span data-stu-id="87bf1-127">**Msvm\_DiskDrive**</span></span>](msvm-diskdrive.md)
</dt> </dl>

 

 




