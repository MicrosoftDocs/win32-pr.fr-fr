---
description: La méthode IsOwnerClearDisabled de la \_ classe TPM Win32 indique si le propriétaire de l’appareil est limité à l’effacement de l’appareil.
ms.assetid: 04f98e9b-c1a0-4828-b7cb-67b32d7470ea
title: Méthode IsOwnerClearDisabled de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnerClearDisabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 13e8b7de707cb1b1af4d4ccdb1208c6391e26987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536521"
---
# <a name="isownercleardisabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="eddda-103">Méthode IsOwnerClearDisabled de la \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="eddda-103">IsOwnerClearDisabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="eddda-104">La méthode **IsOwnerClearDisabled** de la [**classe \_ TPM Win32**](win32-tpm.md) indique si le propriétaire de l’appareil est limité à l’effacement de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="eddda-104">The **IsOwnerClearDisabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device owner is restricted from clearing the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="eddda-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eddda-105">Syntax</span></span>


```mof
uint32 IsOwnerClearDisabled(
  [out] boolean IsOwnerClearDisabled
);
```



## <a name="parameters"></a><span data-ttu-id="eddda-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eddda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eddda-107">*IsOwnerClearDisabled* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="eddda-107">*IsOwnerClearDisabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eddda-108">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="eddda-108">Type: **boolean**</span></span>

<span data-ttu-id="eddda-109">Si la **valeur est true**, le propriétaire de l’appareil ne peut pas effacer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="eddda-109">If **true**, the device owner is unable to clear the device.</span></span> <span data-ttu-id="eddda-110">Seul un utilisateur physiquement présent peut être en mesure de supprimer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="eddda-110">Only a physically present user may be able to clear the device.</span></span> <span data-ttu-id="eddda-111">Si la **valeur est false**, le propriétaire de l’appareil peut effacer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="eddda-111">If **false**, the device owner is able to clear the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eddda-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eddda-112">Return value</span></span>

<span data-ttu-id="eddda-113">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eddda-113">Type: **uint32**</span></span>

<span data-ttu-id="eddda-114">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="eddda-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="eddda-115">Les codes de retour courants sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="eddda-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="eddda-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="eddda-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="eddda-117">Description</span><span class="sxs-lookup"><span data-stu-id="eddda-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="eddda-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="eddda-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="eddda-119">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="eddda-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eddda-120">Notes</span><span class="sxs-lookup"><span data-stu-id="eddda-120">Remarks</span></span>

<span data-ttu-id="eddda-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="eddda-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="eddda-122">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="eddda-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="eddda-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="eddda-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="eddda-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="eddda-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eddda-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eddda-125">Requirements</span></span>



| <span data-ttu-id="eddda-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eddda-126">Requirement</span></span> | <span data-ttu-id="eddda-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="eddda-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="eddda-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eddda-128">Minimum supported client</span></span><br/> | <span data-ttu-id="eddda-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eddda-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="eddda-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eddda-130">Minimum supported server</span></span><br/> | <span data-ttu-id="eddda-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eddda-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="eddda-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="eddda-132">Namespace</span></span><br/>                | <span data-ttu-id="eddda-133">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="eddda-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="eddda-134">MOF</span><span class="sxs-lookup"><span data-stu-id="eddda-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eddda-135"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="eddda-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="eddda-136">DLL</span><span class="sxs-lookup"><span data-stu-id="eddda-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eddda-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="eddda-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eddda-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eddda-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eddda-139">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="eddda-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
