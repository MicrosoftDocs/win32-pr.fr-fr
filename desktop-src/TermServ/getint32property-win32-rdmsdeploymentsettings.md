---
title: Méthode GetInt32Property de la classe Win32_RDMSDeploymentSettings (Microsoft. Diagnostics. appanalysis. h)
description: Récupère une propriété entière pour les paramètres de déploiement d’une collection de bureaux virtuels.
ms.assetid: 6b8174bb-ffb7-4699-a3fb-d32ab0b202fc
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetInt32Property
- Services Bureau à distance de la méthode GetInt32Property, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f96374c610084c8ef7973d4ac4db603d9c28cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510758"
---
# <a name="getint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="7707f-106">Méthode GetInt32Property de la \_ classe Win32 RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="7707f-106">GetInt32Property method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="7707f-107">Récupère une propriété entière pour les paramètres de déploiement d’une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="7707f-107">Retrieves an integer property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7707f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7707f-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="7707f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7707f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7707f-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7707f-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7707f-111">Alias de la collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="7707f-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="7707f-112">*Valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7707f-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7707f-113">Entier qui reçoit la valeur récupérée.</span><span class="sxs-lookup"><span data-stu-id="7707f-113">An integer that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7707f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7707f-114">Requirements</span></span>



| <span data-ttu-id="7707f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7707f-115">Requirement</span></span> | <span data-ttu-id="7707f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7707f-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7707f-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7707f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7707f-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7707f-118">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="7707f-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7707f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7707f-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7707f-120">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="7707f-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7707f-121">Namespace</span></span><br/>                | <span data-ttu-id="7707f-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="7707f-122">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="7707f-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7707f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7707f-124"><dt>Microsoft. Diagnostics. appanalysis. h</dt></span><span class="sxs-lookup"><span data-stu-id="7707f-124"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="7707f-125">MOF</span><span class="sxs-lookup"><span data-stu-id="7707f-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7707f-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7707f-126"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="7707f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7707f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7707f-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7707f-128"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="7707f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7707f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7707f-130">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="7707f-130">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





