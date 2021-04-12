---
description: La méthode IsOwnershipAllowed de la \_ classe TPM Win32 indique si la possibilité d’installer un propriétaire pour l’appareil est autorisée.
ms.assetid: dfeb5afe-4169-470b-b5e4-cf1e5781271e
title: Méthode IsOwnershipAllowed de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnershipAllowed
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: c818d5a4e4eb16ac637372f0c7ed0f2e9211ef88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201349"
---
# <a name="isownershipallowed-method-of-the-win32_tpm-class"></a><span data-ttu-id="90294-103">Méthode IsOwnershipAllowed de la \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="90294-103">IsOwnershipAllowed method of the Win32\_Tpm class</span></span>

<span data-ttu-id="90294-104">La méthode **IsOwnershipAllowed** de la [**classe \_ TPM Win32**](win32-tpm.md) indique si la possibilité d’installer un propriétaire pour l’appareil est autorisée.</span><span class="sxs-lookup"><span data-stu-id="90294-104">The **IsOwnershipAllowed** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the ability to install an owner for the device is permitted.</span></span>

## <a name="syntax"></a><span data-ttu-id="90294-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90294-105">Syntax</span></span>


```mof
uint32 IsOwnershipAllowed(
  [out] boolean IsOwnershipAllowed
);
```



## <a name="parameters"></a><span data-ttu-id="90294-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90294-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90294-107">*IsOwnershipAllowed* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="90294-107">*IsOwnershipAllowed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90294-108">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="90294-108">Type: **boolean**</span></span>

<span data-ttu-id="90294-109">Si la **valeur est true**, la possibilité d’installer un propriétaire pour l’appareil est autorisée.</span><span class="sxs-lookup"><span data-stu-id="90294-109">If **true**, the ability to install an owner for the device is permitted.</span></span> <span data-ttu-id="90294-110">Si la **valeur est false**, la méthode [**TakeOwnership**](takeownership-win32-tpm.md) ne parvient pas à installer un propriétaire pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="90294-110">If **false**, the method [**TakeOwnership**](takeownership-win32-tpm.md) will fail to install an owner for the device.</span></span>

<span data-ttu-id="90294-111">Cette valeur peut être modifiée à l’aide de la méthode [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="90294-111">This value can be changed with the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span> <span data-ttu-id="90294-112">La valeur est réinitialisée à **true** après l’exécution de la méthode [**Clear**](clear-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="90294-112">The value is reset to **true** after the [**Clear**](clear-win32-tpm.md) method is run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90294-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="90294-113">Return value</span></span>

<span data-ttu-id="90294-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="90294-114">Type: **uint32**</span></span>

<span data-ttu-id="90294-115">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="90294-115">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="90294-116">Les codes de retour courants sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="90294-116">Common return codes are listed below.</span></span>



| <span data-ttu-id="90294-117">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="90294-117">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="90294-118">Description</span><span class="sxs-lookup"><span data-stu-id="90294-118">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="90294-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="90294-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="90294-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="90294-120">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="90294-121">Notes</span><span class="sxs-lookup"><span data-stu-id="90294-121">Remarks</span></span>

<span data-ttu-id="90294-122">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="90294-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="90294-123">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="90294-123">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="90294-124">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="90294-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="90294-125">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="90294-125">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="90294-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90294-126">Requirements</span></span>



| <span data-ttu-id="90294-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="90294-127">Requirement</span></span> | <span data-ttu-id="90294-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="90294-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="90294-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90294-129">Minimum supported client</span></span><br/> | <span data-ttu-id="90294-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="90294-130">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="90294-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90294-131">Minimum supported server</span></span><br/> | <span data-ttu-id="90294-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="90294-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="90294-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="90294-133">Namespace</span></span><br/>                | <span data-ttu-id="90294-134">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="90294-134">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="90294-135">MOF</span><span class="sxs-lookup"><span data-stu-id="90294-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90294-136"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="90294-136"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="90294-137">DLL</span><span class="sxs-lookup"><span data-stu-id="90294-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90294-138"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="90294-138"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90294-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90294-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90294-140">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="90294-140">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
