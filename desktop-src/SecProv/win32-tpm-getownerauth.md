---
description: Obtient les informations d’autorisation du propriétaire d’un module de plateforme sécurisée, le cas échéant dans le registre.
ms.assetid: 3E2C28C8-4154-4B1B-9C47-AEDFD5622979
title: 'Win32_Tpm :: GetOwnerAuth, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: a441b07af31758212152b657ccb033d8abdeebbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525666"
---
# <a name="win32_tpmgetownerauth-method"></a><span data-ttu-id="a4b03-103">Win32 \_ TPM :: GetOwnerAuth, méthode</span><span class="sxs-lookup"><span data-stu-id="a4b03-103">Win32\_Tpm::GetOwnerAuth method</span></span>

<span data-ttu-id="a4b03-104">Obtient les informations d’autorisation du propriétaire d’un module de plateforme sécurisée, le cas échéant dans le registre.</span><span class="sxs-lookup"><span data-stu-id="a4b03-104">Gets the owner authorization information for a TPM if one is available in the registry.</span></span> <span data-ttu-id="a4b03-105">Si un module de plateforme sécurisée est détenu ou approvisionné dans Windows 8 avec les paramètres par défaut, les informations d’autorisation du propriétaire du module de plateforme sécurisée sont stockées dans le registre et peuvent être utilisées par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="a4b03-105">If a TPM is owned or provisioned in Windows 8 with the default settings, the TPM owner authorization information is stored in the registry and is available for use by this method.</span></span>

<span data-ttu-id="a4b03-106">Cette méthode est accessible uniquement par les administrateurs locaux.</span><span class="sxs-lookup"><span data-stu-id="a4b03-106">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4b03-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4b03-107">Syntax</span></span>


```C++
uint32 GetOwnerAuth(
  [out] STRING OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="a4b03-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4b03-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4b03-109">*Origine* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a4b03-109">*OwnerAuth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4b03-110">Informations d’autorisation du propriétaire pour un module de plateforme sécurisée (TPM), le cas échéant dans le registre.</span><span class="sxs-lookup"><span data-stu-id="a4b03-110">The owner authorization information for a TPM, if one is available in the registry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4b03-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a4b03-111">Return value</span></span>

<span data-ttu-id="a4b03-112">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux [services de base TPM](../tbs/tbs-return-codes.md) , peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="a4b03-112">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="a4b03-113">Les codes de retour courants sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a4b03-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="a4b03-114">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a4b03-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="a4b03-115">Description</span><span class="sxs-lookup"><span data-stu-id="a4b03-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="a4b03-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="a4b03-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="a4b03-117">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="a4b03-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a4b03-118">Notes</span><span class="sxs-lookup"><span data-stu-id="a4b03-118">Remarks</span></span>

<span data-ttu-id="a4b03-119">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="a4b03-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a4b03-120">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="a4b03-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="a4b03-121">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="a4b03-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a4b03-122">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="a4b03-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b03-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4b03-123">Requirements</span></span>



| <span data-ttu-id="a4b03-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4b03-124">Requirement</span></span> | <span data-ttu-id="a4b03-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4b03-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b03-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4b03-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a4b03-127">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4b03-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a4b03-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4b03-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a4b03-129">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4b03-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a4b03-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a4b03-130">Namespace</span></span><br/>                | <span data-ttu-id="a4b03-131">\\\\.\\ racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="a4b03-131">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="a4b03-132">MOF</span><span class="sxs-lookup"><span data-stu-id="a4b03-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4b03-133"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="a4b03-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4b03-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a4b03-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4b03-135"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="a4b03-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4b03-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4b03-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4b03-137">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="a4b03-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
