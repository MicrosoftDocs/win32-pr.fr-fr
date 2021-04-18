---
title: Méthode SynchronizePublishingData de la classe Win32_RDMSManagementData
description: Synchronise l’ensemble spécifié de données de publication pour Bureau à distance services de gestion (RDMS).
ms.assetid: 0476ce12-9b08-418c-83c2-208275574f5b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SynchronizePublishingData
- Services Bureau à distance de la méthode SynchronizePublishingData, classe Win32_RDMSManagementData
- Win32_RDMSManagementData de la classe Services Bureau à distance, méthode SynchronizePublishingData
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData.SynchronizePublishingData
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d389ad08d81f39cab45502a42f4ebd95e16f36c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384556"
---
# <a name="synchronizepublishingdata-method-of-the-win32_rdmsmanagementdata-class"></a><span data-ttu-id="1688e-106">Méthode SynchronizePublishingData de la \_ classe Win32 RDMSManagementData</span><span class="sxs-lookup"><span data-stu-id="1688e-106">SynchronizePublishingData method of the Win32\_RDMSManagementData class</span></span>

<span data-ttu-id="1688e-107">Synchronise l’ensemble spécifié de données de publication pour Bureau à distance services de gestion (RDMS).</span><span class="sxs-lookup"><span data-stu-id="1688e-107">Synchronizes the specified set of publishing data for Remote Desktop Management Services (RDMS).</span></span>

## <a name="syntax"></a><span data-ttu-id="1688e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1688e-108">Syntax</span></span>


```mof
uint32 SynchronizePublishingData(
  [in] string Context
);
```



## <a name="parameters"></a><span data-ttu-id="1688e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1688e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1688e-110">*Contexte* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1688e-110">*Context* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1688e-111">Informations de contexte des données de publication à synchroniser.</span><span class="sxs-lookup"><span data-stu-id="1688e-111">The context information of the publishing data to synchronize.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1688e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1688e-112">Return value</span></span>

<span data-ttu-id="1688e-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="1688e-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1688e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1688e-114">Requirements</span></span>



| <span data-ttu-id="1688e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1688e-115">Requirement</span></span> | <span data-ttu-id="1688e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1688e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1688e-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1688e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1688e-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1688e-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="1688e-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1688e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1688e-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1688e-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="1688e-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1688e-121">Namespace</span></span><br/>                | <span data-ttu-id="1688e-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="1688e-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="1688e-123">MOF</span><span class="sxs-lookup"><span data-stu-id="1688e-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1688e-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1688e-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="1688e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1688e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1688e-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1688e-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="1688e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1688e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1688e-128">**\_RDMSManagementData Win32**</span><span class="sxs-lookup"><span data-stu-id="1688e-128">**Win32\_RDMSManagementData**</span></span>](win32-rdmsmanagementdata.md)
</dt> </dl>

 

 





