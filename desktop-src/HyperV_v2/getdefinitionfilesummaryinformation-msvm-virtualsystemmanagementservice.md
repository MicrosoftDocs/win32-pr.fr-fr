---
description: Retourne les informations de résumé de l’ordinateur virtuel pour les fichiers de définition d’ordinateur virtuel spécifiés.
ms.assetid: 5a3d7f2c-3b89-4dd6-909d-4452afc3705f
title: Méthode GetDefinitionFileSummaryInformation de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetDefinitionFileSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a46daedd282d07c2367931a9f20a7fbfa1849f9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514644"
---
# <a name="getdefinitionfilesummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="64040-103">Méthode GetDefinitionFileSummaryInformation de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="64040-103">GetDefinitionFileSummaryInformation method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="64040-104">Retourne les informations de résumé de l’ordinateur virtuel pour les fichiers de définition d’ordinateur virtuel spécifiés.</span><span class="sxs-lookup"><span data-stu-id="64040-104">Returns virtual machine summary information for the specified virtual machine definition files.</span></span>

## <a name="syntax"></a><span data-ttu-id="64040-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64040-105">Syntax</span></span>


```mof
uint32 GetDefinitionFileSummaryInformation(
  [in]  string                      DefinitionFiles[],
  [out] Msvm_SummaryInformationBase SummaryInformation[]
);
```



## <a name="parameters"></a><span data-ttu-id="64040-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64040-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64040-107">*DefinitionFiles* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64040-107">*DefinitionFiles* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64040-108">Tableau de chemins d’accès aux fichiers de configuration XML pour lesquels retourner les informations de résumé.</span><span class="sxs-lookup"><span data-stu-id="64040-108">An array of paths to XML configuration files for which to return summary information.</span></span>

</dd> <dt>

<span data-ttu-id="64040-109">*SummaryInformation* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="64040-109">*SummaryInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64040-110">Tableau d’instances [**de \_ SummaryInformationBase MSVM**](msvm-summaryinformation.md) contenant les informations demandées pour les ordinateurs virtuels et/ou les instantanés spécifiés dans le tableau *DefinitionFiles* .</span><span class="sxs-lookup"><span data-stu-id="64040-110">An array of [**Msvm\_SummaryInformationBase**](msvm-summaryinformation.md) instances containing the requested information for the virtual machines and/or snapshots specified in the *DefinitionFiles* array.</span></span> <span data-ttu-id="64040-111">Seules les propriétés **Name**, **ElementName**, **CreationTime** et **Notes** sont retournées, toutes les autres propriétés ont la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="64040-111">Only the **Name**, **ElementName**, **CreationTime**, and **Notes** properties are returned, all other properties will be **Null**.</span></span>

> [!Note]  

 

<span data-ttu-id="64040-112">Avant Windows 10, la version 1703, DataType était [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md).</span><span class="sxs-lookup"><span data-stu-id="64040-112">Prior to Windows 10, version 1703, datatype was [**Msvm\_SummaryInformation**](msvm-summaryinformation.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64040-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="64040-113">Return value</span></span>

<span data-ttu-id="64040-114">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="64040-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="64040-115">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="64040-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="64040-116">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="64040-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="64040-117">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="64040-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="64040-118">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="64040-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="64040-119">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="64040-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="64040-120">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="64040-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="64040-121">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="64040-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="64040-122">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="64040-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="64040-123">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="64040-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="64040-124">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="64040-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="64040-125">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="64040-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="64040-126">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="64040-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="64040-127">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="64040-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="64040-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64040-128">Requirements</span></span>



| <span data-ttu-id="64040-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64040-129">Requirement</span></span> | <span data-ttu-id="64040-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="64040-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64040-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64040-131">Minimum supported client</span></span><br/> | <span data-ttu-id="64040-132">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64040-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="64040-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64040-133">Minimum supported server</span></span><br/> | <span data-ttu-id="64040-134">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64040-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="64040-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="64040-135">Namespace</span></span><br/>                | <span data-ttu-id="64040-136">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="64040-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="64040-137">MOF</span><span class="sxs-lookup"><span data-stu-id="64040-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64040-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64040-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="64040-139">DLL</span><span class="sxs-lookup"><span data-stu-id="64040-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64040-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="64040-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="64040-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64040-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64040-142">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="64040-142">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




