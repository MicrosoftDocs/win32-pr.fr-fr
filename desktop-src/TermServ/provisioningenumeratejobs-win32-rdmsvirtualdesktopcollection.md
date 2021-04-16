---
title: Méthode ProvisioningEnumerateJobs de la classe Win32_RDMSVirtualDesktopCollection
description: Énumère les tâches de provisionnement de bureau virtuel pour ce service.
ms.assetid: 4bd2b03f-ba8c-483e-af09-270424f9b1ed
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ProvisioningEnumerateJobs
- Services Bureau à distance de la méthode ProvisioningEnumerateJobs, classe Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de la classe Services Bureau à distance, méthode ProvisioningEnumerateJobs
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningEnumerateJobs
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa2b54a0599c2bbcaf6b0f9a9acb3ab3028389b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509389"
---
# <a name="provisioningenumeratejobs-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="68aa3-106">Méthode ProvisioningEnumerateJobs de la \_ classe Win32 RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="68aa3-106">ProvisioningEnumerateJobs method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="68aa3-107">Énumère les tâches de provisionnement de bureau virtuel pour ce service.</span><span class="sxs-lookup"><span data-stu-id="68aa3-107">Enumerates virtual desktop provisioning jobs for this service.</span></span>

## <a name="syntax"></a><span data-ttu-id="68aa3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68aa3-108">Syntax</span></span>


```mof
uint32 ProvisioningEnumerateJobs(
  [in]  uint32 JobType,
  [in]  string CollectionAlias,
  [out] string JobGuids[]
);
```



## <a name="parameters"></a><span data-ttu-id="68aa3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68aa3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68aa3-110">*JobType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68aa3-110">*JobType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68aa3-111">Entier qui spécifie le type de travail à énumérer.</span><span class="sxs-lookup"><span data-stu-id="68aa3-111">An integer that specifies the type of job to enumerate.</span></span>

<span data-ttu-id="68aa3-112">Ce paramètre peut être défini sur l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="68aa3-112">This parameter can be set to one of the following values:</span></span>

<dt>

<span data-ttu-id="68aa3-113">0</span><span class="sxs-lookup"><span data-stu-id="68aa3-113">0</span></span>
</dt> <dd>

<span data-ttu-id="68aa3-114">Travaux en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="68aa3-114">Running jobs</span></span>

</dd> <dt>

<span data-ttu-id="68aa3-115">1</span><span class="sxs-lookup"><span data-stu-id="68aa3-115">1</span></span>
</dt> <dd>

<span data-ttu-id="68aa3-116">Travaux terminés</span><span class="sxs-lookup"><span data-stu-id="68aa3-116">Completed jobs</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="68aa3-117">*CollectionAlias* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68aa3-117">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68aa3-118">Alias de la collection de bureaux virtuels à énumérer.</span><span class="sxs-lookup"><span data-stu-id="68aa3-118">The alias of the virtual desktop collection to enumerate.</span></span> <span data-ttu-id="68aa3-119">La valeur par défaut de ce paramètre est FALSe, ce qui indique que tous les travaux en cours d’exécution doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="68aa3-119">The default value for this parameter is FALSE, which specifies that all running jobs are to be enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="68aa3-120">*JobGuids* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="68aa3-120">*JobGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68aa3-121">Tableau qui contient les **GUID** des tâches d’approvisionnement à énumérer.</span><span class="sxs-lookup"><span data-stu-id="68aa3-121">An array that contains the **GUIDs** of provisioning jobs to enumerate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68aa3-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="68aa3-122">Return value</span></span>

<span data-ttu-id="68aa3-123">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="68aa3-123">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="68aa3-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68aa3-124">Requirements</span></span>



| <span data-ttu-id="68aa3-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68aa3-125">Requirement</span></span> | <span data-ttu-id="68aa3-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="68aa3-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="68aa3-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68aa3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="68aa3-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="68aa3-128">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="68aa3-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68aa3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="68aa3-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="68aa3-130">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="68aa3-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="68aa3-131">Namespace</span></span><br/>                | <span data-ttu-id="68aa3-132">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="68aa3-132">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="68aa3-133">MOF</span><span class="sxs-lookup"><span data-stu-id="68aa3-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68aa3-134"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68aa3-134"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="68aa3-135">DLL</span><span class="sxs-lookup"><span data-stu-id="68aa3-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68aa3-136"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68aa3-136"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="68aa3-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68aa3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68aa3-138">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="68aa3-138">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





