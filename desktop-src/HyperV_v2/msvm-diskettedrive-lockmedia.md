---
description: 'Méthode LockMedia de la classe Msvm_DisketteDrive : verrouille ou libère le média.'
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
ms.openlocfilehash: 5f5f87354aa7c39534e8b32c8985c5d18b55caa9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111974"
---
# <a name="lockmedia-method-of-the-msvm_diskettedrive-class"></a><span data-ttu-id="61239-103">Méthode LockMedia de la \_ classe DisketteDrive MSVM</span><span class="sxs-lookup"><span data-stu-id="61239-103">LockMedia method of the Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="61239-104">Verrouille ou libère le média.</span><span class="sxs-lookup"><span data-stu-id="61239-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="61239-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61239-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="61239-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61239-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61239-107">*Verrou* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61239-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61239-108">**true** pour verrouiller le média ; **false** pour libérer le média.</span><span class="sxs-lookup"><span data-stu-id="61239-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61239-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="61239-109">Return value</span></span>

<span data-ttu-id="61239-110">Retourne 0 en cas de réussite ; Sinon, retourne l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="61239-110">Returns a 0 on success; otherwise, returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="61239-111">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="61239-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="61239-112">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="61239-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="61239-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61239-113">Requirements</span></span>



| <span data-ttu-id="61239-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61239-114">Requirement</span></span> | <span data-ttu-id="61239-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="61239-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61239-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61239-116">Minimum supported client</span></span><br/> | <span data-ttu-id="61239-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="61239-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="61239-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61239-118">Minimum supported server</span></span><br/> | <span data-ttu-id="61239-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="61239-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="61239-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="61239-120">Namespace</span></span><br/>                | <span data-ttu-id="61239-121">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="61239-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="61239-122">MOF</span><span class="sxs-lookup"><span data-stu-id="61239-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61239-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61239-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="61239-124">DLL</span><span class="sxs-lookup"><span data-stu-id="61239-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61239-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="61239-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="61239-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61239-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61239-127">**MSVM \_ DisketteDrive**</span><span class="sxs-lookup"><span data-stu-id="61239-127">**Msvm\_DisketteDrive**</span></span>](msvm-diskettedrive.md)
</dt> </dl>

 

 




