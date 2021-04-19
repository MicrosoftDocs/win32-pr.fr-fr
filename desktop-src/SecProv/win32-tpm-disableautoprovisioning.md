---
description: Désactive l’approvisionnement automatique du module de plateforme sécurisée s’il est actuellement activé.
ms.assetid: 30CC2581-9C16-4A11-92F1-625992F2AF20
title: Win32_Tpm ::D méthode isableAutoProvisioning
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.DisableAutoProvisioning
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5387e744ec5f02bf448a997cfe1c8c83342903a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526153"
---
# <a name="win32_tpmdisableautoprovisioning-method"></a><span data-ttu-id="5bc1a-103">\_TPM Win32 ::D méthode isableautoprovisioning</span><span class="sxs-lookup"><span data-stu-id="5bc1a-103">Win32\_Tpm::DisableAutoProvisioning method</span></span>

<span data-ttu-id="5bc1a-104">Désactive l’approvisionnement automatique du module de plateforme sécurisée s’il est actuellement activé.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-104">Disables auto provisioning of the TPM if it is currently enabled.</span></span> <span data-ttu-id="5bc1a-105">L’opération n’a aucun effet si l’approvisionnement automatique est déjà désactivé.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-105">The operation has no effect if auto provisioning is already disabled.</span></span> <span data-ttu-id="5bc1a-106">Par défaut, l’approvisionnement automatique est activé pour Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-106">By default, auto provisioning is enabled for Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="5bc1a-107">Cette méthode est accessible uniquement par les administrateurs locaux.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bc1a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5bc1a-108">Syntax</span></span>


```C++
uint32 DisableAutoProvisioning(
  [in, optional] BOOL OnlyForNextBoot
);
```



## <a name="parameters"></a><span data-ttu-id="5bc1a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5bc1a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bc1a-110">*OnlyForNextBoot* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5bc1a-110">*OnlyForNextBoot* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5bc1a-111">Si la valeur est **true**, l’approvisionnement automatique est désactivé uniquement pour le prochain démarrage.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-111">If set to **TRUE**, auto provisioning is disabled for only the next boot.</span></span> <span data-ttu-id="5bc1a-112">Si la valeur est **false** ou n’est pas spécifié, l’approvisionnement automatique est désactivé définitivement.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-112">If set to **FALSE** or not specified, auto provisioning is permanently disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bc1a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5bc1a-113">Return value</span></span>

<span data-ttu-id="5bc1a-114">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux [services de base TPM](../tbs/tbs-return-codes.md) , peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-114">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="5bc1a-115">Les codes de retour courants sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="5bc1a-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="5bc1a-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="5bc1a-117">Description</span><span class="sxs-lookup"><span data-stu-id="5bc1a-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="5bc1a-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5bc1a-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="5bc1a-119">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5bc1a-120">Notes</span><span class="sxs-lookup"><span data-stu-id="5bc1a-120">Remarks</span></span>

<span data-ttu-id="5bc1a-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="5bc1a-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5bc1a-122">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5bc1a-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="5bc1a-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5bc1a-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5bc1a-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5bc1a-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5bc1a-125">Requirements</span></span>



| <span data-ttu-id="5bc1a-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5bc1a-126">Requirement</span></span> | <span data-ttu-id="5bc1a-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="5bc1a-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bc1a-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5bc1a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5bc1a-129">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5bc1a-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5bc1a-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5bc1a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5bc1a-131">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5bc1a-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5bc1a-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5bc1a-132">Namespace</span></span><br/>                | <span data-ttu-id="5bc1a-133">\\\\.\\ racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="5bc1a-133">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="5bc1a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5bc1a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5bc1a-135"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="5bc1a-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="5bc1a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5bc1a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bc1a-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="5bc1a-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bc1a-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bc1a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bc1a-139">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="5bc1a-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
