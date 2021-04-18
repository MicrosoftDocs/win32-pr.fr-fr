---
title: Méthode SetInt32Property de la classe Win32_RDMSDeploymentSettings
description: Met à jour une propriété entière pour les paramètres de déploiement d’une collection de bureaux virtuels.
ms.assetid: c5e6dbd5-7db7-4409-bf53-c2680e4a5319
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetInt32Property
- Services Bureau à distance de la méthode SetInt32Property, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fecdc42031514d5219fc03172b951602ad021ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106516091"
---
# <a name="setint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="77cd2-106">Méthode SetInt32Property de la \_ classe Win32 RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="77cd2-106">SetInt32Property method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="77cd2-107">Met à jour une propriété entière pour les paramètres de déploiement d’une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="77cd2-107">Updates an integer property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="77cd2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77cd2-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="77cd2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77cd2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77cd2-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77cd2-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77cd2-111">Alias de la collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="77cd2-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="77cd2-112">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77cd2-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77cd2-113">Nouvelle valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="77cd2-113">The new property value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="77cd2-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77cd2-114">Requirements</span></span>



| <span data-ttu-id="77cd2-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77cd2-115">Requirement</span></span> | <span data-ttu-id="77cd2-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="77cd2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="77cd2-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77cd2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="77cd2-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="77cd2-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="77cd2-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77cd2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="77cd2-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="77cd2-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="77cd2-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="77cd2-121">Namespace</span></span><br/>                | <span data-ttu-id="77cd2-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="77cd2-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="77cd2-123">MOF</span><span class="sxs-lookup"><span data-stu-id="77cd2-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77cd2-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77cd2-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="77cd2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="77cd2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77cd2-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77cd2-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="77cd2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77cd2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77cd2-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="77cd2-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





