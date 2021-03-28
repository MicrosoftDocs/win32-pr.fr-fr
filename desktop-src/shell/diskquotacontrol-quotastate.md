---
description: Définit ou obtient l’état des quotas de disque du volume.
title: DiskQuotaControl. QuotaState, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaState
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b0766ecf-6e22-4481-a6a7-df873a277bc2
ms.openlocfilehash: 460decc1068642ae797723b31f7350082f591d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485521"
---
# <a name="diskquotacontrolquotastate-property"></a><span data-ttu-id="fdc1c-103">DiskQuotaControl. QuotaState, propriété</span><span class="sxs-lookup"><span data-stu-id="fdc1c-103">DiskQuotaControl.QuotaState property</span></span>

<span data-ttu-id="fdc1c-104">Définit ou obtient l’état des quotas de disque du volume.</span><span class="sxs-lookup"><span data-stu-id="fdc1c-104">Sets or gets the state of the volume's disk quotas.</span></span>

<span data-ttu-id="fdc1c-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="fdc1c-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdc1c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fdc1c-106">Syntax</span></span>


```JScript
iQuotaState = DiskQuotaControl.QuotaState
DiskQuotaControl.QuotaState = iQuotaState
```



## <a name="property-value"></a><span data-ttu-id="fdc1c-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="fdc1c-107">Property value</span></span>

<span data-ttu-id="fdc1c-108">Cette propriété peut être définie sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="fdc1c-108">This property can be set to one of the following values.</span></span>



| <span data-ttu-id="fdc1c-109">État</span><span class="sxs-lookup"><span data-stu-id="fdc1c-109">State</span></span>          | <span data-ttu-id="fdc1c-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="fdc1c-110">Value</span></span> | <span data-ttu-id="fdc1c-111">Description</span><span class="sxs-lookup"><span data-stu-id="fdc1c-111">Description</span></span>               |
|----------------|-------|---------------------------|
| <span data-ttu-id="fdc1c-112">dqStateDisable</span><span class="sxs-lookup"><span data-stu-id="fdc1c-112">dqStateDisable</span></span> | <span data-ttu-id="fdc1c-113">0</span><span class="sxs-lookup"><span data-stu-id="fdc1c-113">0</span></span>     | <span data-ttu-id="fdc1c-114">Les quotas de disque sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="fdc1c-114">Disk quotas are disabled.</span></span> |
| <span data-ttu-id="fdc1c-115">dqStateTrack</span><span class="sxs-lookup"><span data-stu-id="fdc1c-115">dqStateTrack</span></span>   | <span data-ttu-id="fdc1c-116">1</span><span class="sxs-lookup"><span data-stu-id="fdc1c-116">1</span></span>     | <span data-ttu-id="fdc1c-117">Les quotas de disque sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="fdc1c-117">Disk quotas are disabled.</span></span> |
| <span data-ttu-id="fdc1c-118">dqStateEnforce</span><span class="sxs-lookup"><span data-stu-id="fdc1c-118">dqStateEnforce</span></span> | <span data-ttu-id="fdc1c-119">2</span><span class="sxs-lookup"><span data-stu-id="fdc1c-119">2</span></span>     | <span data-ttu-id="fdc1c-120">Appliquer la limite de quota.</span><span class="sxs-lookup"><span data-stu-id="fdc1c-120">Enforce quota limit.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="fdc1c-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fdc1c-121">Requirements</span></span>



| <span data-ttu-id="fdc1c-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fdc1c-122">Requirement</span></span> | <span data-ttu-id="fdc1c-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="fdc1c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdc1c-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fdc1c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fdc1c-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fdc1c-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fdc1c-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fdc1c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fdc1c-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fdc1c-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fdc1c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="fdc1c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdc1c-129"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="fdc1c-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdc1c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fdc1c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdc1c-131">**Objet DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="fdc1c-131">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




