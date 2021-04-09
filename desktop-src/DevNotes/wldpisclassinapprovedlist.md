---
description: Appelle la bibliothèque pour valider si un CLSID particulier peut être appelé en toute sécurité.
ms.assetid: 94C8731B-88FD-4240-BF5D-2CD67C41B063
title: WldpIsClassInApprovedList, fonction (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsClassInApprovedList
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 01762c60a3f1aef1574cc218ace9988669175efe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110071"
---
# <a name="wldpisclassinapprovedlist-function"></a><span data-ttu-id="b40a6-103">WldpIsClassInApprovedList fonction)</span><span class="sxs-lookup"><span data-stu-id="b40a6-103">WldpIsClassInApprovedList function</span></span>

<span data-ttu-id="b40a6-104">Appelle la bibliothèque pour valider si un **CLSID** particulier peut être appelé en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="b40a6-104">Calls the library to validate if a particular **CLSID** is safe to be called.</span></span> <span data-ttu-id="b40a6-105">La fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="b40a6-105">The function has no associated import library.</span></span> <span data-ttu-id="b40a6-106">Vous devez utiliser les fonctions LoadLibrary et GetProcAddress pour établir une liaison dynamique à wldp.dll.</span><span class="sxs-lookup"><span data-stu-id="b40a6-106">You must use the LoadLibrary and GetProcAddress functions to dynamically link to wldp.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="b40a6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b40a6-107">Syntax</span></span>


```C++
HRESULT WINAPI WldpIsClassInApprovedList(
        REFCLSID               classID,
  _In_  PWLDP_HOST_INFORMATION hostInformation,
  _Out_ PBOOL                  isApproved,
        DWORD                  optionalFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b40a6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b40a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b40a6-109">*classID*</span><span class="sxs-lookup"><span data-stu-id="b40a6-109">*classID*</span></span> 
</dt> <dd>

<span data-ttu-id="b40a6-110">ID de classe COM pour lequel vérifier l’approbation.</span><span class="sxs-lookup"><span data-stu-id="b40a6-110">The COM class ID to check for approval.</span></span>

</dd> <dt>

<span data-ttu-id="b40a6-111">*hostInformation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b40a6-111">*hostInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b40a6-112">Structure [**d' \_ \_ informations de l’hôte WLDP**](wldp-host-information.md) identifiant l’hôte à évaluer.</span><span class="sxs-lookup"><span data-stu-id="b40a6-112">A [**WLDP\_HOST\_INFORMATION**](wldp-host-information.md) structure identifying the host to be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="b40a6-113">*IsApproved* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b40a6-113">*isApproved* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b40a6-114">En cas de réussite de l’opération, contient la **valeur true** si l’ID de classe est approuvé ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="b40a6-114">On successful completion, contains **TRUE** if the class ID is approved; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b40a6-115">*optionalFlags*</span><span class="sxs-lookup"><span data-stu-id="b40a6-115">*optionalFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="b40a6-116">Ce paramètre est réservé et doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="b40a6-116">This parameter is reserved and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b40a6-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b40a6-117">Return value</span></span>

<span data-ttu-id="b40a6-118">Cette méthode retourne **S \_ OK** en cas de réussite ou un code d’échec dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b40a6-118">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b40a6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b40a6-119">Requirements</span></span>



| <span data-ttu-id="b40a6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b40a6-120">Requirement</span></span> | <span data-ttu-id="b40a6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b40a6-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b40a6-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b40a6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b40a6-123">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b40a6-123">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b40a6-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b40a6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b40a6-125">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b40a6-125">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b40a6-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="b40a6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b40a6-127"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b40a6-127"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b40a6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b40a6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b40a6-129"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b40a6-129"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




