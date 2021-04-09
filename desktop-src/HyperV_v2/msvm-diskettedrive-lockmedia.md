---
description: Verrouille ou libère le média.
ms.assetid: 90f7e06c-92d0-4742-a74d-68ae6bfc00bf
title: Méthode LockMedia de la classe Msvm_DisketteDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4f9bce4e9e46d76c3426271af16c28026c242fa9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869533"
---
# <a name="lockmedia-method-of-the-msvm_diskettedrive-class"></a><span data-ttu-id="ffa5f-103">Méthode LockMedia de la \_ classe DisketteDrive MSVM</span><span class="sxs-lookup"><span data-stu-id="ffa5f-103">LockMedia method of the Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="ffa5f-104">Verrouille ou libère le média.</span><span class="sxs-lookup"><span data-stu-id="ffa5f-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffa5f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffa5f-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="ffa5f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ffa5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffa5f-107">*Verrou* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ffa5f-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffa5f-108">**true** pour verrouiller le média ; **false** pour libérer le média.</span><span class="sxs-lookup"><span data-stu-id="ffa5f-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffa5f-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ffa5f-109">Return value</span></span>

<span data-ttu-id="ffa5f-110">Retourne 0 en cas de réussite ; Sinon, retourne l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ffa5f-110">Returns a 0 on success; otherwise, returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="ffa5f-111">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="ffa5f-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ffa5f-112">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="ffa5f-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ffa5f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffa5f-113">Requirements</span></span>



| <span data-ttu-id="ffa5f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffa5f-114">Requirement</span></span> | <span data-ttu-id="ffa5f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffa5f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffa5f-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffa5f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ffa5f-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ffa5f-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ffa5f-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffa5f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ffa5f-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ffa5f-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ffa5f-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ffa5f-120">Namespace</span></span><br/>                | <span data-ttu-id="ffa5f-121">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ffa5f-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ffa5f-122">MOF</span><span class="sxs-lookup"><span data-stu-id="ffa5f-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffa5f-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffa5f-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffa5f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ffa5f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffa5f-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ffa5f-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ffa5f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffa5f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffa5f-127">**MSVM \_ DisketteDrive**</span><span class="sxs-lookup"><span data-stu-id="ffa5f-127">**Msvm\_DisketteDrive**</span></span>](msvm-diskettedrive.md)
</dt> </dl>

 

 




