---
description: La méthode IsOwned de la \_ classe TPM Win32 indique si l’appareil a un propriétaire. Cette valeur est modifiée par la méthode TakeOwnership.
ms.assetid: 04a9394f-98de-43e3-8a19-7a8f409823b8
title: Méthode IsOwned de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwned
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6ad2d7d03059d8f96fe726d50ea18c2a70db64f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525677"
---
# <a name="isowned-method-of-the-win32_tpm-class"></a><span data-ttu-id="75f50-104">Méthode IsOwned de la \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="75f50-104">IsOwned method of the Win32\_Tpm class</span></span>

<span data-ttu-id="75f50-105">La méthode **IsOwned** de la [**classe \_ TPM Win32**](win32-tpm.md) indique si l’appareil a un propriétaire.</span><span class="sxs-lookup"><span data-stu-id="75f50-105">The **IsOwned** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device has an owner.</span></span> <span data-ttu-id="75f50-106">Cette valeur est modifiée par la méthode [**TakeOwnership**](takeownership-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="75f50-106">This value is changed by the [**TakeOwnership**](takeownership-win32-tpm.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="75f50-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75f50-107">Syntax</span></span>


```mof
uint32 IsOwned(
  [out] boolean IsOwned
);
```



## <a name="parameters"></a><span data-ttu-id="75f50-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75f50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75f50-109">*IsOwned* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="75f50-109">*IsOwned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75f50-110">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="75f50-110">Type: **boolean**</span></span>

<span data-ttu-id="75f50-111">Si la **valeur est true**, l’appareil a un propriétaire.</span><span class="sxs-lookup"><span data-stu-id="75f50-111">If **true**, the device has an owner.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75f50-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="75f50-112">Return value</span></span>

<span data-ttu-id="75f50-113">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="75f50-113">Type: **uint32**</span></span>

<span data-ttu-id="75f50-114">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="75f50-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="75f50-115">Les codes de retour courants sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="75f50-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="75f50-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="75f50-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="75f50-117">Description</span><span class="sxs-lookup"><span data-stu-id="75f50-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="75f50-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="75f50-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="75f50-119">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="75f50-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="75f50-120">Notes</span><span class="sxs-lookup"><span data-stu-id="75f50-120">Remarks</span></span>

<span data-ttu-id="75f50-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="75f50-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="75f50-122">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="75f50-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="75f50-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="75f50-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="75f50-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="75f50-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="75f50-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75f50-125">Requirements</span></span>



| <span data-ttu-id="75f50-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75f50-126">Requirement</span></span> | <span data-ttu-id="75f50-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="75f50-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="75f50-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75f50-128">Minimum supported client</span></span><br/> | <span data-ttu-id="75f50-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75f50-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="75f50-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75f50-130">Minimum supported server</span></span><br/> | <span data-ttu-id="75f50-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75f50-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="75f50-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="75f50-132">Namespace</span></span><br/>                | <span data-ttu-id="75f50-133">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="75f50-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="75f50-134">MOF</span><span class="sxs-lookup"><span data-stu-id="75f50-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75f50-135"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="75f50-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="75f50-136">DLL</span><span class="sxs-lookup"><span data-stu-id="75f50-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75f50-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="75f50-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75f50-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75f50-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75f50-139">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="75f50-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
