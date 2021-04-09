---
description: Indique si l’approvisionnement automatique du module de plateforme sécurisée est activé.
ms.assetid: C908673C-8BDB-4541-85C6-65FED1EBB535
title: 'Win32_Tpm :: IsAutoProvisioningEnabled, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsAutoProvisioningEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: cb269247292646464c6126a2588a50d77b19db9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866946"
---
# <a name="win32_tpmisautoprovisioningenabled-method"></a><span data-ttu-id="f7e34-103">Win32 \_ TPM :: IsAutoProvisioningEnabled, méthode</span><span class="sxs-lookup"><span data-stu-id="f7e34-103">Win32\_Tpm::IsAutoProvisioningEnabled method</span></span>

<span data-ttu-id="f7e34-104">Indique si l’approvisionnement automatique du module de plateforme sécurisée est activé.</span><span class="sxs-lookup"><span data-stu-id="f7e34-104">Indicates if auto provisioning of the TPM is enabled.</span></span> <span data-ttu-id="f7e34-105">Par défaut, l’approvisionnement automatique est activé pour Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="f7e34-105">By default, auto provisioning is enabled for Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="f7e34-106">Cette méthode est accessible uniquement par les administrateurs locaux.</span><span class="sxs-lookup"><span data-stu-id="f7e34-106">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7e34-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7e34-107">Syntax</span></span>


```C++
uint32 IsAutoProvisioningEnabled(
  [out] BOOL IsAutoProvisioningEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="f7e34-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7e34-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7e34-109">*IsAutoProvisioningEnabled* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f7e34-109">*IsAutoProvisioningEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7e34-110">Affectez la valeur **true** si l’approvisionnement automatique du module de plateforme sécurisée est activé.</span><span class="sxs-lookup"><span data-stu-id="f7e34-110">Set to **TRUE** if the TPM auto provisioning is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7e34-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f7e34-111">Return value</span></span>

<span data-ttu-id="f7e34-112">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux [services de base TPM](../tbs/tbs-return-codes.md) , peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="f7e34-112">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="f7e34-113">Les codes de retour courants sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="f7e34-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="f7e34-114">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f7e34-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="f7e34-115">Description</span><span class="sxs-lookup"><span data-stu-id="f7e34-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="f7e34-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f7e34-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="f7e34-117">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="f7e34-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f7e34-118">Notes</span><span class="sxs-lookup"><span data-stu-id="f7e34-118">Remarks</span></span>

<span data-ttu-id="f7e34-119">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="f7e34-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f7e34-120">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="f7e34-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f7e34-121">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="f7e34-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f7e34-122">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f7e34-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7e34-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7e34-123">Requirements</span></span>



| <span data-ttu-id="f7e34-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7e34-124">Requirement</span></span> | <span data-ttu-id="f7e34-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7e34-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7e34-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7e34-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f7e34-127">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7e34-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f7e34-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7e34-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f7e34-129">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7e34-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f7e34-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f7e34-130">Namespace</span></span><br/>                | <span data-ttu-id="f7e34-131">\\\\.\\ racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="f7e34-131">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="f7e34-132">MOF</span><span class="sxs-lookup"><span data-stu-id="f7e34-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7e34-133"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="f7e34-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7e34-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f7e34-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7e34-135"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="f7e34-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7e34-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7e34-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7e34-137">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="f7e34-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
