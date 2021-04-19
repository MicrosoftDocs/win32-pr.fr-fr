---
description: Retourne une chaîne de message d’erreur mise en forme pour le tableau spécifié d’instances d’erreur MSVM incorporées \_ .
ms.assetid: 477EF4AE-00A8-4F2D-A335-E41A2EF620BB
title: Méthode FormatError de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.FormatError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e768a6ea968d428d7809c7c322a80f3ad233aa2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531668"
---
# <a name="formaterror-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="a39b1-103">Méthode FormatError de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="a39b1-103">FormatError method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="a39b1-104">Retourne une chaîne de message d’erreur mise en forme pour le tableau spécifié d’instances d' [**\_ erreur MSVM**](msvm-error.md) incorporées.</span><span class="sxs-lookup"><span data-stu-id="a39b1-104">Returns a formatted error message string for the specified array of embedded [**Msvm\_Error**](msvm-error.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="a39b1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a39b1-105">Syntax</span></span>


```mof
uint32 FormatError(
  [in]  string Errors[],
  [out] string ErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="a39b1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a39b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a39b1-107">*Erreurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a39b1-107">*Errors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a39b1-108">Type : **chaîne \[ \]**</span><span class="sxs-lookup"><span data-stu-id="a39b1-108">Type: **string\[\]**</span></span>

<span data-ttu-id="a39b1-109">Tableau de chaînes contenant les instances d' [**\_ erreur MSVM**](msvm-error.md) utilisées pour générer le message d’erreur de sortie.</span><span class="sxs-lookup"><span data-stu-id="a39b1-109">An array of strings containing [**Msvm\_Error**](msvm-error.md) instances used to generate the output error message.</span></span>

</dd> <dt>

<span data-ttu-id="a39b1-110">*ErrorMessage* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a39b1-110">*ErrorMessage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a39b1-111">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a39b1-111">Type: **string**</span></span>

<span data-ttu-id="a39b1-112">Lors de la sortie, chaîne qui contient les messages d’erreur concaténés représentés par les instances d' [**\_ erreur MSVM**](msvm-error.md) passées dans le paramètre *Errors* .</span><span class="sxs-lookup"><span data-stu-id="a39b1-112">On output, a string that contains the concatenated error messages represented by the [**Msvm\_Error**](msvm-error.md) instances passed in the *Errors* parameter.</span></span> <span data-ttu-id="a39b1-113">Chaque chaîne d’erreur est séparée par une paire de caractères de saut de ligne (' \\ n').</span><span class="sxs-lookup"><span data-stu-id="a39b1-113">Each error string is separated by a pair of newline characters ('\\n').</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a39b1-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a39b1-114">Return value</span></span>

<span data-ttu-id="a39b1-115">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a39b1-115">Type: **uint32**</span></span>

<span data-ttu-id="a39b1-116">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a39b1-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a39b1-117">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="a39b1-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a39b1-118">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="a39b1-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a39b1-119">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="a39b1-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a39b1-120">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="a39b1-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a39b1-121">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="a39b1-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a39b1-122">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="a39b1-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a39b1-123">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="a39b1-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a39b1-124">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="a39b1-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a39b1-125">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="a39b1-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a39b1-126">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="a39b1-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a39b1-127">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="a39b1-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a39b1-128">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="a39b1-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a39b1-129">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="a39b1-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="a39b1-130">Notes</span><span class="sxs-lookup"><span data-stu-id="a39b1-130">Remarks</span></span>

<span data-ttu-id="a39b1-131">L’accès à la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="a39b1-131">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a39b1-132">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a39b1-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a39b1-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a39b1-133">Requirements</span></span>



| <span data-ttu-id="a39b1-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a39b1-134">Requirement</span></span> | <span data-ttu-id="a39b1-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="a39b1-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a39b1-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a39b1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a39b1-137">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a39b1-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a39b1-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a39b1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a39b1-139">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a39b1-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a39b1-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a39b1-140">Namespace</span></span><br/>                | <span data-ttu-id="a39b1-141">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a39b1-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a39b1-142">MOF</span><span class="sxs-lookup"><span data-stu-id="a39b1-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a39b1-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a39b1-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a39b1-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a39b1-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a39b1-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a39b1-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a39b1-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a39b1-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a39b1-147">**FormatError (v1)**</span><span class="sxs-lookup"><span data-stu-id="a39b1-147">**FormatError (V1)**</span></span>](/previous-versions/windows/desktop/virtual/formaterror-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="a39b1-148">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="a39b1-148">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

