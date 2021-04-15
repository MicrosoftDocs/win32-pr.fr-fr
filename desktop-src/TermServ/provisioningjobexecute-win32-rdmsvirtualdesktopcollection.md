---
title: Méthode ProvisioningJobExecute de la classe Win32_RDMSVirtualDesktopCollection
description: Exécute un travail d’approvisionnement de bureau virtuel.
ms.assetid: 69f0cc6a-7eef-4cd9-94ac-f0c7e52d02d8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ProvisioningJobExecute
- Services Bureau à distance de la méthode ProvisioningJobExecute, classe Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de la classe Services Bureau à distance, méthode ProvisioningJobExecute
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobExecute
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c632a6bdc5fc5c4a128941d8a6c8b4379ddf9629
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466743"
---
# <a name="provisioningjobexecute-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="a0fda-106">Méthode ProvisioningJobExecute de la \_ classe Win32 RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="a0fda-106">ProvisioningJobExecute method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="a0fda-107">Exécute un travail d’approvisionnement de bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="a0fda-107">Runs a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0fda-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0fda-108">Syntax</span></span>


```mof
uint32 ProvisioningJobExecute(
  [in]  string JobInputXml,
  [out] string JobGuid
);
```



## <a name="parameters"></a><span data-ttu-id="a0fda-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0fda-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0fda-110">*JobInputXml* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a0fda-110">*JobInputXml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0fda-111">Chaîne qui contient les informations de configuration au format XML.</span><span class="sxs-lookup"><span data-stu-id="a0fda-111">A string that contains the provisioning information in XML format.</span></span>

</dd> <dt>

<span data-ttu-id="a0fda-112">*JobGuid* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a0fda-112">*JobGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0fda-113">**GUID** qui identifie de façon unique le travail d’approvisionnement à exécuter.</span><span class="sxs-lookup"><span data-stu-id="a0fda-113">The **GUID** that uniquely identifies the provisioning job to run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0fda-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a0fda-114">Return value</span></span>

<span data-ttu-id="a0fda-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="a0fda-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0fda-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0fda-116">Requirements</span></span>



| <span data-ttu-id="a0fda-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0fda-117">Requirement</span></span> | <span data-ttu-id="a0fda-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0fda-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0fda-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0fda-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a0fda-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0fda-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="a0fda-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0fda-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a0fda-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a0fda-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="a0fda-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a0fda-123">Namespace</span></span><br/>                | <span data-ttu-id="a0fda-124">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="a0fda-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="a0fda-125">MOF</span><span class="sxs-lookup"><span data-stu-id="a0fda-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0fda-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0fda-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0fda-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a0fda-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0fda-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0fda-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="a0fda-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0fda-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0fda-130">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="a0fda-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





