---
description: Récupère le mode sécurisé Windows actuel. Les fenêtres peuvent être en mode verrouillé, en mode normal déverrouillé ou en mode d’évaluation.
ms.assetid: FD280818-C6DE-4CEA-A772-E239A8DB891F
title: WldpQueryWindowsLockdownMode, fonction (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryWindowsLockdownMode
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: fc746270a0634525154417cfba7e1529bee7edfb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201080"
---
# <a name="wldpquerywindowslockdownmode-function"></a><span data-ttu-id="84e00-104">WldpQueryWindowsLockdownMode fonction)</span><span class="sxs-lookup"><span data-stu-id="84e00-104">WldpQueryWindowsLockdownMode function</span></span>

<span data-ttu-id="84e00-105">Récupère le mode sécurisé Windows actuel.</span><span class="sxs-lookup"><span data-stu-id="84e00-105">Retrieves the current Windows secure mode.</span></span> <span data-ttu-id="84e00-106">Les fenêtres peuvent être en mode verrouillé, en mode normal déverrouillé ou en mode d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="84e00-106">Windows can be in locked mode, unlocked normal mode, or trial mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="84e00-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84e00-107">Syntax</span></span>


```C++
 WINAPI WldpQueryWindowsLockdownMode(
  _Out_ PWLDP_WINDOWS_LOCKDOWN_MODE lockdownMode
);
```



## <a name="parameters"></a><span data-ttu-id="84e00-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84e00-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84e00-109">*lockdownMode* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="84e00-109">*lockdownMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84e00-110">En cas de réussite, retourne un [**\_ \_ \_ mode de verrouillage Windows PWLDP**](wldp-windows-lockdown-mode.md) qui indique le mode sécurisé pour l’appareil Windows 10 actuel.</span><span class="sxs-lookup"><span data-stu-id="84e00-110">On success, returns a [**PWLDP\_WINDOWS\_LOCKDOWN\_MODE**](wldp-windows-lockdown-mode.md) that indicates the secure mode for the current Windows 10 device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84e00-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="84e00-111">Return value</span></span>

<span data-ttu-id="84e00-112">Cette méthode retourne **S \_ OK** en cas de réussite ou un code d’échec dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="84e00-112">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="84e00-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84e00-113">Requirements</span></span>



| <span data-ttu-id="84e00-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84e00-114">Requirement</span></span> | <span data-ttu-id="84e00-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="84e00-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="84e00-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84e00-116">Minimum supported client</span></span><br/> | <span data-ttu-id="84e00-117">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84e00-117">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="84e00-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84e00-118">Minimum supported server</span></span><br/> | <span data-ttu-id="84e00-119">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84e00-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="84e00-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="84e00-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="84e00-121"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="84e00-121"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="84e00-122">DLL</span><span class="sxs-lookup"><span data-stu-id="84e00-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84e00-123"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84e00-123"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




