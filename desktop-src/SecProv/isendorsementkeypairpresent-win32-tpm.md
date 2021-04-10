---
description: La méthode IsEndorsementKeyPairPresent de la \_ classe TPM Win32 indique si la paire de clés de type EK existe sur l’appareil.
ms.assetid: c36cd0b5-1ac2-4fcf-b140-c5ecb0b3b211
title: Méthode IsEndorsementKeyPairPresent de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEndorsementKeyPairPresent
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 63561a4971523fd1554e1d973861c3f0737df2ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115871"
---
# <a name="isendorsementkeypairpresent-method-of-the-win32_tpm-class"></a><span data-ttu-id="d4472-103">Méthode IsEndorsementKeyPairPresent de la \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="d4472-103">IsEndorsementKeyPairPresent method of the Win32\_Tpm class</span></span>

<span data-ttu-id="d4472-104">La méthode **IsEndorsementKeyPairPresent** de la [**classe \_ TPM Win32**](win32-tpm.md) indique si la paire de clés de type EK existe sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d4472-104">The **IsEndorsementKeyPairPresent** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the endorsement key pair exists on the device.</span></span> <span data-ttu-id="d4472-105">La paire de clés de type EK est nécessaire pour que l’appareil puisse être détenu.</span><span class="sxs-lookup"><span data-stu-id="d4472-105">The endorsement key pair is required before the device can be owned.</span></span> <span data-ttu-id="d4472-106">Cette paire de clés peut être créée par la méthode [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="d4472-106">This key pair can be created by the [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) method.</span></span>

<span data-ttu-id="d4472-107">L’appareil doit être activé et activé pour que cette méthode aboutisse.</span><span class="sxs-lookup"><span data-stu-id="d4472-107">The device must be enabled and activated for this method to succeed.</span></span> <span data-ttu-id="d4472-108">Pour activer et activer un appareil sans propriétaire, consultez la méthode [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="d4472-108">To enable and activate an unowned device, see the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4472-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4472-109">Syntax</span></span>


```mof
uint32 IsEndorsementKeyPairPresent(
  [out] boolean IsEndorsementKeyPairPresent
);
```



## <a name="parameters"></a><span data-ttu-id="d4472-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4472-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4472-111">*IsEndorsementKeyPairPresent* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d4472-111">*IsEndorsementKeyPairPresent* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4472-112">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d4472-112">Type: **boolean**</span></span>

<span data-ttu-id="d4472-113">Si la **valeur est true**, la paire de clés de type EK existe sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d4472-113">If **true**, the endorsement key pair exists on the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4472-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d4472-114">Return value</span></span>

<span data-ttu-id="d4472-115">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4472-115">Type: **uint32**</span></span>

<span data-ttu-id="d4472-116">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="d4472-116">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="d4472-117">Les codes de retour courants sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d4472-117">Common return codes are listed below.</span></span>



| <span data-ttu-id="d4472-118">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d4472-118">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="d4472-119">Description</span><span class="sxs-lookup"><span data-stu-id="d4472-119">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="d4472-120"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="d4472-120"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="d4472-121">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="d4472-121">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d4472-122">Notes</span><span class="sxs-lookup"><span data-stu-id="d4472-122">Remarks</span></span>

<span data-ttu-id="d4472-123">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="d4472-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d4472-124">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="d4472-124">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="d4472-125">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="d4472-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d4472-126">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="d4472-126">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4472-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4472-127">Requirements</span></span>



| <span data-ttu-id="d4472-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4472-128">Requirement</span></span> | <span data-ttu-id="d4472-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4472-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4472-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4472-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d4472-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4472-131">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d4472-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4472-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d4472-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4472-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d4472-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d4472-134">Namespace</span></span><br/>                | <span data-ttu-id="d4472-135">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="d4472-135">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="d4472-136">MOF</span><span class="sxs-lookup"><span data-stu-id="d4472-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4472-137"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="d4472-137"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4472-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d4472-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4472-139"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="d4472-139"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4472-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4472-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4472-141">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="d4472-141">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="d4472-142">**CreateEndorsementKeyPair**</span><span class="sxs-lookup"><span data-stu-id="d4472-142">**CreateEndorsementKeyPair**</span></span>](createendorsementkeypair-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="d4472-143">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="d4472-143">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
