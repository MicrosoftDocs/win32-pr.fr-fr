---
description: La méthode IsSrkAuthCompatible de la \_ classe TPM Win32 indique si l’autorisation de clé de racine de stockage (SRK) est compatible avec la valeur attendue par Windows Vista.
ms.assetid: ce6d05b8-673a-40ab-a1d7-3fedfd099306
title: Méthode IsSrkAuthCompatible de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsSrkAuthCompatible
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: f5250f8d3f9ad38f9d4c46350e06e0fe32f756dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866957"
---
# <a name="issrkauthcompatible-method-of-the-win32_tpm-class"></a><span data-ttu-id="eaf6b-103">Méthode IsSrkAuthCompatible de la \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="eaf6b-103">IsSrkAuthCompatible method of the Win32\_Tpm class</span></span>

<span data-ttu-id="eaf6b-104">La méthode **IsSrkAuthCompatible** de la [**classe \_ TPM Win32**](win32-tpm.md) indique si l’autorisation de clé de racine de stockage (SRK) est compatible avec la valeur attendue par Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-104">The **IsSrkAuthCompatible** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the Storage Root Key (SRK) authorization is compatible with the value expected by Windows Vista.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaf6b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eaf6b-105">Syntax</span></span>


```mof
uint32 IsSrkAuthCompatible(
  [out] boolean IsSrkAuthCompatible
);
```



## <a name="parameters"></a><span data-ttu-id="eaf6b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eaf6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaf6b-107">*IsSrkAuthCompatible* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="eaf6b-107">*IsSrkAuthCompatible* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eaf6b-108">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="eaf6b-108">Type: **boolean**</span></span>

<span data-ttu-id="eaf6b-109">Si la valeur est **true**, la valeur d’autorisation SRK a une valeur égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-109">If **true**, the SRK authorization value has a value of zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaf6b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eaf6b-110">Return value</span></span>

<span data-ttu-id="eaf6b-111">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eaf6b-111">Type: **uint32**</span></span>

<span data-ttu-id="eaf6b-112">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="eaf6b-113">Les codes de retour courants sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="eaf6b-114">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="eaf6b-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="eaf6b-115">Description</span><span class="sxs-lookup"><span data-stu-id="eaf6b-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="eaf6b-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="eaf6b-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="eaf6b-117">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eaf6b-118">Notes</span><span class="sxs-lookup"><span data-stu-id="eaf6b-118">Remarks</span></span>

<span data-ttu-id="eaf6b-119">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="eaf6b-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="eaf6b-120">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="eaf6b-121">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="eaf6b-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="eaf6b-122">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="eaf6b-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eaf6b-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eaf6b-123">Requirements</span></span>



| <span data-ttu-id="eaf6b-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eaf6b-124">Requirement</span></span> | <span data-ttu-id="eaf6b-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="eaf6b-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf6b-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eaf6b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="eaf6b-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eaf6b-127">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="eaf6b-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eaf6b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="eaf6b-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eaf6b-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="eaf6b-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="eaf6b-130">Namespace</span></span><br/>                | <span data-ttu-id="eaf6b-131">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="eaf6b-131">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="eaf6b-132">MOF</span><span class="sxs-lookup"><span data-stu-id="eaf6b-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eaf6b-133"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="eaf6b-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="eaf6b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="eaf6b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaf6b-135"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="eaf6b-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaf6b-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eaf6b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaf6b-137">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="eaf6b-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
