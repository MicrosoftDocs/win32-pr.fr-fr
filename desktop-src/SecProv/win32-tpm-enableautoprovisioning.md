---
description: Active l’approvisionnement automatique du module de plateforme sécurisée s’il est actuellement désactivé.
ms.assetid: 70F56A4C-F936-4CB6-83F6-F3B691F43B98
title: 'Win32_Tpm :: EnableAutoProvisioning, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.EnableAutoProvisioning
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5288be5c9822b7e76b0cb25b60ee68dacc36d5e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318202"
---
# <a name="win32_tpmenableautoprovisioning-method"></a><span data-ttu-id="98f60-103">Win32 \_ TPM :: EnableAutoProvisioning, méthode</span><span class="sxs-lookup"><span data-stu-id="98f60-103">Win32\_Tpm::EnableAutoProvisioning method</span></span>

<span data-ttu-id="98f60-104">Active l’approvisionnement automatique du module de plateforme sécurisée s’il est actuellement désactivé.</span><span class="sxs-lookup"><span data-stu-id="98f60-104">Enables auto provisioning of the TPM if it is currently disabled.</span></span> <span data-ttu-id="98f60-105">L’opération n’a aucun effet si l’approvisionnement automatique est déjà activé.</span><span class="sxs-lookup"><span data-stu-id="98f60-105">The operation has no effect if auto provisioning is already enabled.</span></span> <span data-ttu-id="98f60-106">Par défaut, l’approvisionnement automatique est activé pour Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="98f60-106">By default, auto provisioning is enabled for Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="98f60-107">Cette méthode est accessible uniquement par les administrateurs locaux.</span><span class="sxs-lookup"><span data-stu-id="98f60-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="98f60-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98f60-108">Syntax</span></span>


```C++
uint32 EnableAutoProvisioning();
```



## <a name="parameters"></a><span data-ttu-id="98f60-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98f60-109">Parameters</span></span>

<span data-ttu-id="98f60-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="98f60-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="98f60-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="98f60-111">Return value</span></span>

<span data-ttu-id="98f60-112">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux [services de base TPM](../tbs/tbs-return-codes.md) , peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="98f60-112">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="98f60-113">Les codes de retour courants sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="98f60-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="98f60-114">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="98f60-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="98f60-115">Description</span><span class="sxs-lookup"><span data-stu-id="98f60-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="98f60-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="98f60-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="98f60-117">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="98f60-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="98f60-118">Notes</span><span class="sxs-lookup"><span data-stu-id="98f60-118">Remarks</span></span>

<span data-ttu-id="98f60-119">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="98f60-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="98f60-120">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="98f60-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="98f60-121">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="98f60-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="98f60-122">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="98f60-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="98f60-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98f60-123">Requirements</span></span>



| <span data-ttu-id="98f60-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98f60-124">Requirement</span></span> | <span data-ttu-id="98f60-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="98f60-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="98f60-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98f60-126">Minimum supported client</span></span><br/> | <span data-ttu-id="98f60-127">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98f60-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="98f60-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98f60-128">Minimum supported server</span></span><br/> | <span data-ttu-id="98f60-129">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98f60-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="98f60-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="98f60-130">Namespace</span></span><br/>                | <span data-ttu-id="98f60-131">\\\\.\\ racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="98f60-131">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="98f60-132">MOF</span><span class="sxs-lookup"><span data-stu-id="98f60-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98f60-133"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="98f60-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="98f60-134">DLL</span><span class="sxs-lookup"><span data-stu-id="98f60-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98f60-135"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="98f60-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98f60-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98f60-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98f60-137">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="98f60-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
