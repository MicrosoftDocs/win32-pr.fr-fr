---
title: Méthode ProvisioningJobCancel de la classe Win32_RDMSVirtualDesktopCollection
description: Annule un travail d’approvisionnement de bureau virtuel.
ms.assetid: 933ea0f3-b916-4e70-89de-597f9eb23976
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ProvisioningJobCancel
- Services Bureau à distance de la méthode ProvisioningJobCancel, classe Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de la classe Services Bureau à distance, méthode ProvisioningJobCancel
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobCancel
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f414bcdc264d682817898bae98fcf60a716452
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509532"
---
# <a name="provisioningjobcancel-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="9d6e4-106">Méthode ProvisioningJobCancel de la \_ classe Win32 RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="9d6e4-106">ProvisioningJobCancel method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="9d6e4-107">Annule un travail d’approvisionnement de bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="9d6e4-107">Cancels a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d6e4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d6e4-108">Syntax</span></span>


```mof
uint32 ProvisioningJobCancel(
  [in] string JobGuid
);
```



## <a name="parameters"></a><span data-ttu-id="9d6e4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d6e4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d6e4-110">*JobGuid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9d6e4-110">*JobGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d6e4-111">**GUID** qui identifie de façon unique le travail d’approvisionnement à annuler.</span><span class="sxs-lookup"><span data-stu-id="9d6e4-111">The **GUID** that uniquely identifies the provisioning job to cancel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d6e4-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d6e4-112">Return value</span></span>

<span data-ttu-id="9d6e4-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="9d6e4-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d6e4-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d6e4-114">Requirements</span></span>



| <span data-ttu-id="9d6e4-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d6e4-115">Requirement</span></span> | <span data-ttu-id="9d6e4-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d6e4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d6e4-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d6e4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9d6e4-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d6e4-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="9d6e4-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d6e4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9d6e4-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9d6e4-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="9d6e4-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9d6e4-121">Namespace</span></span><br/>                | <span data-ttu-id="9d6e4-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="9d6e4-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="9d6e4-123">MOF</span><span class="sxs-lookup"><span data-stu-id="9d6e4-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d6e4-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d6e4-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d6e4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9d6e4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d6e4-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d6e4-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="9d6e4-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d6e4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d6e4-128">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="9d6e4-128">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





