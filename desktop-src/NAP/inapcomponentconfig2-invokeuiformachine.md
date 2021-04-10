---
title: Méthode INapComponentConfig2 InvokeUIForMachine (NapCommon. h)
description: Est implémenté par les validateurs d’intégrité système (SHV) si nécessaire pour gérer la configuration distante directement sur l’ordinateur spécifié. Cette méthode lance une interface utilisateur de gestion de la configuration.
ms.assetid: 67a6d715-250b-4b8b-9c27-8173926b7bfe
keywords:
- Méthode InvokeUIForMachine NAP
- Méthode InvokeUIForMachine NAP, interface INapComponentConfig2
- INapComponentConfig2 interface NAP, méthode InvokeUIForMachine
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIForMachine
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bc0c09f802a63a5bfad92b49f76fcbb4ee242d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103540"
---
# <a name="inapcomponentconfig2invokeuiformachine-method"></a><span data-ttu-id="aec9d-107">INapComponentConfig2 :: InvokeUIForMachine, méthode</span><span class="sxs-lookup"><span data-stu-id="aec9d-107">INapComponentConfig2::InvokeUIForMachine method</span></span>

> [!Note]  
> <span data-ttu-id="aec9d-108">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="aec9d-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="aec9d-109">La méthode **InvokeUIForMachine** est implémentée par les validateurs d’intégrité système (SHV) si nécessaire pour gérer la configuration distante directement sur l’ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="aec9d-109">The **InvokeUIForMachine** method is implemented by system health validators (SHVs) as needed to manage remote configuration directly on the machine specified.</span></span> <span data-ttu-id="aec9d-110">Cette méthode lance une interface utilisateur de gestion de la configuration.</span><span class="sxs-lookup"><span data-stu-id="aec9d-110">This method launches a configuration management UI.</span></span>

## <a name="syntax"></a><span data-ttu-id="aec9d-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aec9d-111">Syntax</span></span>


```C++
HRESULT InvokeUIForMachine(
  [in] HWND          hwndParent,
  [in] CountedString *machineName
);
```



## <a name="parameters"></a><span data-ttu-id="aec9d-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aec9d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aec9d-113">*hwndParent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aec9d-113">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aec9d-114">Handle de la fenêtre parente ou propriétaire.</span><span class="sxs-lookup"><span data-stu-id="aec9d-114">A handle to the parent or owner window.</span></span> <span data-ttu-id="aec9d-115">Un handle de fenêtre valide doit être fourni.</span><span class="sxs-lookup"><span data-stu-id="aec9d-115">A valid window handle must be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="aec9d-116">*nomordinateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aec9d-116">*machineName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aec9d-117">Pointeur vers un [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) qui contient le nom de l’ordinateur du client NAP.</span><span class="sxs-lookup"><span data-stu-id="aec9d-117">A pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) that contains the machine name of the NAP client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aec9d-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aec9d-118">Return value</span></span>

<span data-ttu-id="aec9d-119">Retourne S \_ OK en cas de réussite, ou l’un des codes d’erreur Windows standard.</span><span class="sxs-lookup"><span data-stu-id="aec9d-119">Returns S\_OK if successful, or one of the standard Windows error codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="aec9d-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aec9d-120">Requirements</span></span>



| <span data-ttu-id="aec9d-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aec9d-121">Requirement</span></span> | <span data-ttu-id="aec9d-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="aec9d-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aec9d-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aec9d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="aec9d-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="aec9d-124">None supported</span></span><br/>                                                                |
| <span data-ttu-id="aec9d-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aec9d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="aec9d-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aec9d-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="aec9d-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="aec9d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="aec9d-128"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="aec9d-128"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="aec9d-129">MIDL</span><span class="sxs-lookup"><span data-stu-id="aec9d-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aec9d-130"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="aec9d-130"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aec9d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aec9d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aec9d-132">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="aec9d-132">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> </dl>

 

 





