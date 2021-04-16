---
description: La méthode IsPhysicalPresenceHardwareEnabled de la \_ classe TPM Win32 indique si la présence physique sur la plateforme peut être définie à l’aide d’un signal matériel.
ms.assetid: 65dabfa9-bfbe-4b9b-8e80-02269895c7ad
title: Méthode IsPhysicalPresenceHardwareEnabled de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsPhysicalPresenceHardwareEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 674dcaa733d8ec70af172359e3dcde0578955dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393492"
---
# <a name="isphysicalpresencehardwareenabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="959b2-103">Méthode IsPhysicalPresenceHardwareEnabled de la \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="959b2-103">IsPhysicalPresenceHardwareEnabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="959b2-104">La méthode **IsPhysicalPresenceHardwareEnabled** de la [**classe \_ TPM Win32**](win32-tpm.md) indique si la présence physique sur la plateforme peut être définie à l’aide d’un signal matériel.</span><span class="sxs-lookup"><span data-stu-id="959b2-104">The **IsPhysicalPresenceHardwareEnabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether physical presence on the platform can be set with a hardware signal.</span></span> <span data-ttu-id="959b2-105">Cette valeur est configurée par le fabricant de la plateforme en fonction de la conception de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="959b2-105">This value is configured by the platform manufacturer based on the design of the platform.</span></span> <span data-ttu-id="959b2-106">La documentation du fabricant de la plateforme peut fournir des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="959b2-106">Documentation from the platform manufacturer may provide additional information.</span></span>

## <a name="syntax"></a><span data-ttu-id="959b2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="959b2-107">Syntax</span></span>


```mof
uint32 IsPhysicalPresenceHardwareEnabled(
  [out] boolean IsPhysicalPresenceHardwareEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="959b2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="959b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="959b2-109">*IsPhysicalPresenceHardwareEnabled* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="959b2-109">*IsPhysicalPresenceHardwareEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="959b2-110">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="959b2-110">Type: **boolean**</span></span>

<span data-ttu-id="959b2-111">Si la **valeur est true**, la présence physique sur la plateforme peut être définie à l’aide d’un signal matériel.</span><span class="sxs-lookup"><span data-stu-id="959b2-111">If **true**, physical presence on the platform can be set with a hardware signal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="959b2-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="959b2-112">Return value</span></span>

<span data-ttu-id="959b2-113">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="959b2-113">Type: **uint32**</span></span>

<span data-ttu-id="959b2-114">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="959b2-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="959b2-115">Les codes de retour courants sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="959b2-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="959b2-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="959b2-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="959b2-117">Description</span><span class="sxs-lookup"><span data-stu-id="959b2-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="959b2-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="959b2-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="959b2-119">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="959b2-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="959b2-120">Notes</span><span class="sxs-lookup"><span data-stu-id="959b2-120">Remarks</span></span>

<span data-ttu-id="959b2-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="959b2-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="959b2-122">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="959b2-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="959b2-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="959b2-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="959b2-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="959b2-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="959b2-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="959b2-125">Requirements</span></span>



| <span data-ttu-id="959b2-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="959b2-126">Requirement</span></span> | <span data-ttu-id="959b2-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="959b2-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="959b2-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="959b2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="959b2-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="959b2-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="959b2-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="959b2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="959b2-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="959b2-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="959b2-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="959b2-132">Namespace</span></span><br/>                | <span data-ttu-id="959b2-133">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="959b2-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="959b2-134">MOF</span><span class="sxs-lookup"><span data-stu-id="959b2-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="959b2-135"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="959b2-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="959b2-136">DLL</span><span class="sxs-lookup"><span data-stu-id="959b2-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="959b2-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="959b2-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="959b2-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="959b2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="959b2-139">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="959b2-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
