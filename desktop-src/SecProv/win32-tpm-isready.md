---
description: Indique si le module de plateforme sécurisée est prêt à être utilisé.
ms.assetid: 70E9EB90-DC13-4431-97E5-D77B4E345373
title: 'Win32_Tpm :: IsReady, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsReady
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 37c9d579e424c89f8670838b09ed1c557514ca00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525665"
---
# <a name="win32_tpmisready-method"></a><span data-ttu-id="73403-103">Win32 \_ TPM :: IsReady, méthode</span><span class="sxs-lookup"><span data-stu-id="73403-103">Win32\_Tpm::IsReady method</span></span>

<span data-ttu-id="73403-104">Indique si le module de plateforme sécurisée est prêt à être utilisé.</span><span class="sxs-lookup"><span data-stu-id="73403-104">Indicates whether the TPM is ready for use.</span></span>

<span data-ttu-id="73403-105">Cette méthode est accessible uniquement par les administrateurs locaux.</span><span class="sxs-lookup"><span data-stu-id="73403-105">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="73403-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73403-106">Syntax</span></span>


```C++
uint32 IsReady(
  [out] BOOL IsReady
);
```



## <a name="parameters"></a><span data-ttu-id="73403-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73403-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73403-108">*IsReady* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="73403-108">*IsReady* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73403-109">Affectez la valeur **true** si le module de plateforme sécurisée et le système sont entièrement approvisionnés pour une utilisation TPM.</span><span class="sxs-lookup"><span data-stu-id="73403-109">Set to **TRUE** if the TPM and system are fully provisioned for TPM use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73403-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="73403-110">Return value</span></span>

<span data-ttu-id="73403-111">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux [services de base TPM](../tbs/tbs-return-codes.md) , peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="73403-111">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="73403-112">Les codes de retour courants sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="73403-112">Common return codes are listed below.</span></span>



| <span data-ttu-id="73403-113">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="73403-113">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="73403-114">Description</span><span class="sxs-lookup"><span data-stu-id="73403-114">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="73403-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="73403-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="73403-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="73403-116">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="73403-117">Notes</span><span class="sxs-lookup"><span data-stu-id="73403-117">Remarks</span></span>

<span data-ttu-id="73403-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="73403-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="73403-119">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="73403-119">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="73403-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="73403-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="73403-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="73403-121">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="73403-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73403-122">Requirements</span></span>



| <span data-ttu-id="73403-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73403-123">Requirement</span></span> | <span data-ttu-id="73403-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="73403-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="73403-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73403-125">Minimum supported client</span></span><br/> | <span data-ttu-id="73403-126">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73403-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="73403-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73403-127">Minimum supported server</span></span><br/> | <span data-ttu-id="73403-128">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73403-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="73403-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="73403-129">Namespace</span></span><br/>                | <span data-ttu-id="73403-130">\\\\.\\ racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="73403-130">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="73403-131">MOF</span><span class="sxs-lookup"><span data-stu-id="73403-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73403-132"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="73403-132"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="73403-133">DLL</span><span class="sxs-lookup"><span data-stu-id="73403-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73403-134"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="73403-134"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73403-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73403-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73403-136">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="73403-136">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
