---
description: Verrouille ou libère le média.
ms.assetid: 924bc20a-901b-4618-be49-eaacf80c9465
title: Méthode LockMedia de la classe Msvm_DVDDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DVDDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 650a868d8e25e2ccc47271e49634827fe7d3d967
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104116078"
---
# <a name="lockmedia-method-of-the-msvm_dvddrive-class"></a><span data-ttu-id="50391-103">Méthode LockMedia de la \_ classe DVDDrive MSVM</span><span class="sxs-lookup"><span data-stu-id="50391-103">LockMedia method of the Msvm\_DVDDrive class</span></span>

<span data-ttu-id="50391-104">Verrouille ou libère le média.</span><span class="sxs-lookup"><span data-stu-id="50391-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="50391-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50391-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="50391-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50391-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50391-107">*Verrou* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="50391-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50391-108">**true** pour verrouiller le média ; **false** pour libérer le média.</span><span class="sxs-lookup"><span data-stu-id="50391-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50391-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="50391-109">Return value</span></span>

<span data-ttu-id="50391-110">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="50391-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="50391-111">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="50391-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="50391-112">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="50391-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="50391-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50391-113">Requirements</span></span>



| <span data-ttu-id="50391-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50391-114">Requirement</span></span> | <span data-ttu-id="50391-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="50391-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50391-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50391-116">Minimum supported client</span></span><br/> | <span data-ttu-id="50391-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="50391-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="50391-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50391-118">Minimum supported server</span></span><br/> | <span data-ttu-id="50391-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="50391-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="50391-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="50391-120">Namespace</span></span><br/>                | <span data-ttu-id="50391-121">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="50391-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="50391-122">MOF</span><span class="sxs-lookup"><span data-stu-id="50391-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50391-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="50391-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="50391-124">DLL</span><span class="sxs-lookup"><span data-stu-id="50391-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50391-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="50391-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="50391-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50391-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50391-127">**MSVM \_ DVDDrive**</span><span class="sxs-lookup"><span data-stu-id="50391-127">**Msvm\_DVDDrive**</span></span>](msvm-dvddrive.md)
</dt> </dl>

 

 




