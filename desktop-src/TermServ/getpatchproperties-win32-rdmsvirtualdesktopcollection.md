---
title: Méthode GetPatchProperties de la classe Win32_RDMSVirtualDesktopCollection
description: Récupère les propriétés d’un travail d’approvisionnement des mises à jour logicielles pour les machines virtuelles dans une collection de bureaux virtuels.
ms.assetid: 9f228d89-0613-49c7-8169-48491c3a2d9b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetPatchProperties
- Services Bureau à distance de la méthode GetPatchProperties, classe Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de la classe Services Bureau à distance, méthode GetPatchProperties
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetPatchProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f0ca45c97512818aa5f8a9ea851d18fa5554c32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508846"
---
# <a name="getpatchproperties-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="237bc-106">Méthode GetPatchProperties de la \_ classe Win32 RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="237bc-106">GetPatchProperties method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="237bc-107">Récupère les propriétés d’un travail d’approvisionnement des mises à jour logicielles pour les machines virtuelles dans une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="237bc-107">Retrieves the properties of a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="237bc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="237bc-108">Syntax</span></span>


```mof
uint32 GetPatchProperties(
  [out] DATETIME StartTime,
  [out] DATETIME ForceLogOffTime,
  [out] string   JobGuid,
  [out] uint32   State
);
```



## <a name="parameters"></a><span data-ttu-id="237bc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="237bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="237bc-110">*StartTime* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="237bc-110">*StartTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="237bc-111">Date et heure d’installation des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="237bc-111">The date and time to install the updates.</span></span>

</dd> <dt>

<span data-ttu-id="237bc-112">*ForceLogOffTime* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="237bc-112">*ForceLogOffTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="237bc-113">Date et heure auxquelles le système déconnecte les utilisateurs des ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="237bc-113">The date and time on which the system will log off users of the virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="237bc-114">*JobGuid* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="237bc-114">*JobGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="237bc-115">**GUID** qui identifie de façon unique le travail d’approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="237bc-115">A **GUID** that uniquely identifies the provisioning job.</span></span>

</dd> <dt>

<span data-ttu-id="237bc-116">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="237bc-116">*State* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="237bc-117">État du travail d’approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="237bc-117">The state of the provisioning job.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="237bc-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="237bc-118">Return value</span></span>

<span data-ttu-id="237bc-119">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="237bc-119">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="237bc-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="237bc-120">Requirements</span></span>



| <span data-ttu-id="237bc-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="237bc-121">Requirement</span></span> | <span data-ttu-id="237bc-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="237bc-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="237bc-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="237bc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="237bc-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="237bc-124">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="237bc-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="237bc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="237bc-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="237bc-126">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="237bc-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="237bc-127">Namespace</span></span><br/>                | <span data-ttu-id="237bc-128">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="237bc-128">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="237bc-129">MOF</span><span class="sxs-lookup"><span data-stu-id="237bc-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="237bc-130"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="237bc-130"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="237bc-131">DLL</span><span class="sxs-lookup"><span data-stu-id="237bc-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="237bc-132"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="237bc-132"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="237bc-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="237bc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="237bc-134">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="237bc-134">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





