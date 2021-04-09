---
description: Récupère une valeur qui décrit l’état d’application de la stratégie Device Guard pour le code dynamique .NET.
ms.assetid: 11E6C631-0FF8-4DB2-931A-1012B3CA4357
title: WldpIsDynamicCodePolicyEnabled, fonction (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsDynamicCodePolicyEnabled
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 4df0555f89e9c575a7d97b69a5252c17936eb3d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110070"
---
# <a name="wldpisdynamiccodepolicyenabled-function"></a><span data-ttu-id="cd565-103">WldpIsDynamicCodePolicyEnabled fonction)</span><span class="sxs-lookup"><span data-stu-id="cd565-103">WldpIsDynamicCodePolicyEnabled function</span></span>

<span data-ttu-id="cd565-104">Récupère une valeur qui décrit l’état d’application de la stratégie Device Guard pour le code dynamique .NET.</span><span class="sxs-lookup"><span data-stu-id="cd565-104">Retrieves a value that describes the Device Guard policy enforcement status for .NET dynamic code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd565-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd565-105">Syntax</span></span>


```C++
HRESULT WINAPI WldpIsDynamicCodePolicyEnabled(
  _Out_ PBOOL  isEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="cd565-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd565-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd565-107">*IsEnabled* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cd565-107">*isEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd565-108">En cas de réussite, retourne la **valeur true** si la stratégie Device Guard applique la stratégie de code dynamique .net ; Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="cd565-108">On success, returns **true** if the Device Guard policy enforces .NET Dynamic Code policy; otherwise, returns **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd565-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cd565-109">Return value</span></span>

<span data-ttu-id="cd565-110">Cette méthode retourne **S \_ OK** en cas de réussite ou un code d’échec dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="cd565-110">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd565-111">Notes</span><span class="sxs-lookup"><span data-stu-id="cd565-111">Remarks</span></span>

<span data-ttu-id="cd565-112">Le code dynamique fait référence au code généré dynamiquement par la liste de révocation de certificats .NET.</span><span class="sxs-lookup"><span data-stu-id="cd565-112">Dynamic code refers to .NET CRL dynamically-generated code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd565-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd565-113">Requirements</span></span>



| <span data-ttu-id="cd565-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd565-114">Requirement</span></span> | <span data-ttu-id="cd565-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd565-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cd565-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd565-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cd565-117">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd565-117">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cd565-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd565-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cd565-119">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd565-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cd565-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="cd565-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd565-121"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd565-121"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cd565-122">DLL</span><span class="sxs-lookup"><span data-stu-id="cd565-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd565-123"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd565-123"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




