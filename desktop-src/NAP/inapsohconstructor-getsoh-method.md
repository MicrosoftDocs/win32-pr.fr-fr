---
title: Méthode INapSoHConstructor GetSoH (NapProtocol. h)
description: Récupère le paquet SoHRequest ou SoHResponse construit.
ms.assetid: 402c72fd-9e23-453a-8c95-57615295e056
keywords:
- Méthode GetSoH NAP
- Méthode GetSoH NAP, interface INapSoHConstructor
- INapSoHConstructor interface NAP, méthode GetSoH
topic_type:
- apiref
api_name:
- INapSoHConstructor.GetSoH
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066257aadf0ed14816efec06936d4b070087159f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103537"
---
# <a name="inapsohconstructorgetsoh-method"></a><span data-ttu-id="577a6-106">INapSoHConstructor :: GetSoH, méthode</span><span class="sxs-lookup"><span data-stu-id="577a6-106">INapSoHConstructor::GetSoH method</span></span>

> [!Note]  
> <span data-ttu-id="577a6-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="577a6-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="577a6-108">La méthode **INapSoHConstructor :: GetSoH** récupère le paquet SoHRequest ou SoHResponse construit.</span><span class="sxs-lookup"><span data-stu-id="577a6-108">The **INapSoHConstructor::GetSoH** method retrieves the constructed SoHRequest or SoHResponse packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="577a6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="577a6-109">Syntax</span></span>


```C++
HRESULT GetSoH(
  [out] SoH **soh
);
```



## <a name="parameters"></a><span data-ttu-id="577a6-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="577a6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="577a6-111">*SOH* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="577a6-111">*soh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="577a6-112">Pointeur vers un pointeur vers le paquet [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) ou **SoHResponse** construit.</span><span class="sxs-lookup"><span data-stu-id="577a6-112">A pointer to a pointer to the constructed [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) or **SoHResponse** packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="577a6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="577a6-113">Return value</span></span>

<span data-ttu-id="577a6-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="577a6-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="577a6-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="577a6-115">Return code</span></span>                                                                                     | <span data-ttu-id="577a6-116">Description</span><span class="sxs-lookup"><span data-stu-id="577a6-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="577a6-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="577a6-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="577a6-118">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="577a6-118">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="577a6-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="577a6-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="577a6-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="577a6-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="577a6-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="577a6-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="577a6-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="577a6-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="577a6-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="577a6-123">Requirements</span></span>



| <span data-ttu-id="577a6-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="577a6-124">Requirement</span></span> | <span data-ttu-id="577a6-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="577a6-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="577a6-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="577a6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="577a6-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="577a6-127">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="577a6-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="577a6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="577a6-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="577a6-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="577a6-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="577a6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="577a6-131"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="577a6-131"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="577a6-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="577a6-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="577a6-133"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="577a6-133"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="577a6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="577a6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="577a6-135"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="577a6-135"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="577a6-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="577a6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="577a6-137">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="577a6-137">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





