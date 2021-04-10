---
description: Importe les informations d’autorisation du propriétaire pour un module de plateforme sécurisée qui est déjà détenu dans le Registre du système d’exploitation.
ms.assetid: 9611D363-6F10-48B9-B417-97133E975257
title: 'Win32_Tpm :: ImportOwnerAuth, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ImportOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: c74d99ab5cf101aa424dcf1921da774f53e21de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951076"
---
# <a name="win32_tpmimportownerauth-method"></a><span data-ttu-id="fb436-103">Win32 \_ TPM :: ImportOwnerAuth, méthode</span><span class="sxs-lookup"><span data-stu-id="fb436-103">Win32\_Tpm::ImportOwnerAuth method</span></span>

<span data-ttu-id="fb436-104">Importe les informations d’autorisation du propriétaire pour un module de plateforme sécurisée qui est déjà détenu dans le Registre du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="fb436-104">Imports the owner authorization information for a TPM that is already owned into the operating system registry.</span></span> <span data-ttu-id="fb436-105">Cette opération va tout d’abord vérifier si les informations d’autorisation du propriétaire fournies sont correctes.</span><span class="sxs-lookup"><span data-stu-id="fb436-105">This operation will first validate if the supplied owner authorization information is correct.</span></span> <span data-ttu-id="fb436-106">Si elle est correcte, la méthode importe ces informations dans le registre.</span><span class="sxs-lookup"><span data-stu-id="fb436-106">If correct, the method imports this information to the registry.</span></span>

<span data-ttu-id="fb436-107">Cette méthode est accessible uniquement par les administrateurs locaux.</span><span class="sxs-lookup"><span data-stu-id="fb436-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb436-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb436-108">Syntax</span></span>


```C++
uint32 ImportOwnerAuth(
  [in] STRING OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="fb436-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb436-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb436-110">*Origine* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb436-110">*OwnerAuth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb436-111">Informations d’autorisation du propriétaire valides pour le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="fb436-111">The valid owner authorization information for the TPM.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb436-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fb436-112">Return value</span></span>

<span data-ttu-id="fb436-113">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux [services de base TPM](../tbs/tbs-return-codes.md) , peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="fb436-113">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="fb436-114">Les codes de retour courants sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="fb436-114">Common return codes are listed below.</span></span>



| <span data-ttu-id="fb436-115">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="fb436-115">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="fb436-116">Description</span><span class="sxs-lookup"><span data-stu-id="fb436-116">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="fb436-117"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="fb436-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="fb436-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="fb436-118">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fb436-119">Notes</span><span class="sxs-lookup"><span data-stu-id="fb436-119">Remarks</span></span>

<span data-ttu-id="fb436-120">Cette méthode est particulièrement utile dans les scénarios où le module de plateforme sécurisée est dans un état « prêt à fonctionner avec des fonctionnalités réduites » et nécessite que l’importation de l’autorisation du propriétaire soit entièrement prête ou dans un scénario à double démarrage où l’un des systèmes d’exploitation possédait le TPM et que les informations d’autorisation du propriétaire du module de plateforme sécurisée ne sont pas disponibles</span><span class="sxs-lookup"><span data-stu-id="fb436-120">This method is particularly useful in the scenarios where the TPM is in a "ready with reduced functionality state " and requires the importing of the owner authorization to be fully ready or in a dual-boot scenarios where one of the operating systems has owned the TPM and the owner authorization information for TPM is not available in the other operating system.</span></span>

<span data-ttu-id="fb436-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="fb436-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fb436-122">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="fb436-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="fb436-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="fb436-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fb436-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="fb436-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb436-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb436-125">Requirements</span></span>



| <span data-ttu-id="fb436-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb436-126">Requirement</span></span> | <span data-ttu-id="fb436-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb436-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb436-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb436-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fb436-129">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb436-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fb436-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb436-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fb436-131">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb436-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="fb436-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fb436-132">Namespace</span></span><br/>                | <span data-ttu-id="fb436-133">\\\\.\\ racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="fb436-133">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="fb436-134">MOF</span><span class="sxs-lookup"><span data-stu-id="fb436-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb436-135"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="fb436-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb436-136">DLL</span><span class="sxs-lookup"><span data-stu-id="fb436-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb436-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="fb436-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb436-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb436-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb436-139">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="fb436-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
