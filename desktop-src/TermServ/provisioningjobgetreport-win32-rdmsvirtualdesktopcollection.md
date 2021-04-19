---
title: Méthode ProvisioningJobGetReport de la classe Win32_RDMSVirtualDesktopCollection
description: Obtient un rapport sur l’état d’un travail d’approvisionnement de bureaux virtuels.
ms.assetid: 8fc03fed-0838-4530-9b0f-0f561d76769d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ProvisioningJobGetReport
- Services Bureau à distance de la méthode ProvisioningJobGetReport, classe Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de la classe Services Bureau à distance, méthode ProvisioningJobGetReport
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobGetReport
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6605402c6ed6c0269b9971922bdefd48f265c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509110"
---
# <a name="provisioningjobgetreport-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="3ddcc-106">Méthode ProvisioningJobGetReport de la \_ classe Win32 RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="3ddcc-106">ProvisioningJobGetReport method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="3ddcc-107">Obtient un rapport sur l’état d’un travail d’approvisionnement de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="3ddcc-107">Gets a report about the status of a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ddcc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ddcc-108">Syntax</span></span>


```mof
uint32 ProvisioningJobGetReport(
  [in]  string JobGuid,
  [out] string JobReportXml
);
```



## <a name="parameters"></a><span data-ttu-id="3ddcc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ddcc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ddcc-110">*JobGuid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3ddcc-110">*JobGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ddcc-111">**GUID** qui identifie de façon unique le travail d’approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="3ddcc-111">The **GUID** that uniquely identifies the provisioning job.</span></span>

</dd> <dt>

<span data-ttu-id="3ddcc-112">*JobReportXml* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3ddcc-112">*JobReportXml* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ddcc-113">Chaîne qui contient le rapport au format XML.</span><span class="sxs-lookup"><span data-stu-id="3ddcc-113">A string that contains the report in XML format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ddcc-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3ddcc-114">Return value</span></span>

<span data-ttu-id="3ddcc-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="3ddcc-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ddcc-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ddcc-116">Requirements</span></span>



| <span data-ttu-id="3ddcc-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ddcc-117">Requirement</span></span> | <span data-ttu-id="3ddcc-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ddcc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ddcc-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ddcc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3ddcc-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ddcc-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="3ddcc-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ddcc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3ddcc-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3ddcc-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="3ddcc-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3ddcc-123">Namespace</span></span><br/>                | <span data-ttu-id="3ddcc-124">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="3ddcc-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="3ddcc-125">MOF</span><span class="sxs-lookup"><span data-stu-id="3ddcc-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ddcc-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ddcc-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ddcc-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3ddcc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ddcc-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ddcc-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="3ddcc-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ddcc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ddcc-130">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="3ddcc-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





