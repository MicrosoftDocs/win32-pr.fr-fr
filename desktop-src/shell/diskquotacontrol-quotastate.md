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
ms.openlocfilehash: 3580ad47a5ec6a5d0276dc0e30a4a6463aca2fb3
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843190"
---
# <a name="diskquotacontrolquotastate-property"></a><span data-ttu-id="bfcf2-103">DiskQuotaControl. QuotaState, propriété</span><span class="sxs-lookup"><span data-stu-id="bfcf2-103">DiskQuotaControl.QuotaState property</span></span>

<span data-ttu-id="bfcf2-104">Définit ou obtient l’état des quotas de disque du volume.</span><span class="sxs-lookup"><span data-stu-id="bfcf2-104">Sets or gets the state of the volume's disk quotas.</span></span>

<span data-ttu-id="bfcf2-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="bfcf2-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfcf2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfcf2-106">Syntax</span></span>


```JScript
iQuotaState = DiskQuotaControl.QuotaState
DiskQuotaControl.QuotaState = iQuotaState
```



## <a name="property-value"></a><span data-ttu-id="bfcf2-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="bfcf2-107">Property value</span></span>

<span data-ttu-id="bfcf2-108">Cette propriété peut être définie sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="bfcf2-108">This property can be set to one of the following values.</span></span>



| <span data-ttu-id="bfcf2-109">État</span><span class="sxs-lookup"><span data-stu-id="bfcf2-109">State</span></span>          | <span data-ttu-id="bfcf2-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfcf2-110">Value</span></span> | <span data-ttu-id="bfcf2-111">Description</span><span class="sxs-lookup"><span data-stu-id="bfcf2-111">Description</span></span>               |
|----------------|-------|---------------------------|
| <span data-ttu-id="bfcf2-112">dqStateDisable</span><span class="sxs-lookup"><span data-stu-id="bfcf2-112">dqStateDisable</span></span> | <span data-ttu-id="bfcf2-113">0</span><span class="sxs-lookup"><span data-stu-id="bfcf2-113">0</span></span>     | <span data-ttu-id="bfcf2-114">Les quotas de disque sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="bfcf2-114">Disk quotas are disabled.</span></span> |
| <span data-ttu-id="bfcf2-115">dqStateTrack</span><span class="sxs-lookup"><span data-stu-id="bfcf2-115">dqStateTrack</span></span>   | <span data-ttu-id="bfcf2-116">1</span><span class="sxs-lookup"><span data-stu-id="bfcf2-116">1</span></span>     | <span data-ttu-id="bfcf2-117">Les quotas de disque sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="bfcf2-117">Disk quotas are disabled.</span></span> |
| <span data-ttu-id="bfcf2-118">dqStateEnforce</span><span class="sxs-lookup"><span data-stu-id="bfcf2-118">dqStateEnforce</span></span> | <span data-ttu-id="bfcf2-119">2</span><span class="sxs-lookup"><span data-stu-id="bfcf2-119">2</span></span>     | <span data-ttu-id="bfcf2-120">Appliquer la limite de quota.</span><span class="sxs-lookup"><span data-stu-id="bfcf2-120">Enforce quota limit.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="bfcf2-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bfcf2-121">Requirements</span></span>



| <span data-ttu-id="bfcf2-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bfcf2-122">Requirement</span></span> | <span data-ttu-id="bfcf2-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfcf2-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfcf2-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfcf2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bfcf2-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bfcf2-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bfcf2-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfcf2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bfcf2-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bfcf2-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="bfcf2-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bfcf2-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfcf2-129"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="bfcf2-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfcf2-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfcf2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfcf2-131">**Objet DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="bfcf2-131">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




