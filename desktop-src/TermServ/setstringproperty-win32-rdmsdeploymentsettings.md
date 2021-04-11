---
title: Méthode SetStringProperty de la classe Win32_RDMSDeploymentSettings (certenroll. h)
description: Met à jour une propriété de type chaîne pour les paramètres de déploiement d’une collection de bureaux virtuels.
ms.assetid: 500ab1cb-7336-47a8-adee-790976ea30fe
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetStringProperty
- Services Bureau à distance de la méthode SetStringProperty, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode SetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 138f6d91ed428caabf8da69e3d958675f879dd15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104605"
---
# <a name="setstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="bf25a-106">Méthode SetStringProperty de la \_ classe Win32 RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="bf25a-106">SetStringProperty method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="bf25a-107">Met à jour une propriété de type chaîne pour les paramètres de déploiement d’une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="bf25a-107">Updates a string property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf25a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf25a-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="bf25a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf25a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf25a-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf25a-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf25a-111">Alias de la collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="bf25a-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="bf25a-112">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf25a-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf25a-113">Nouvelle valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="bf25a-113">The new property value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf25a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf25a-114">Requirements</span></span>



| <span data-ttu-id="bf25a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf25a-115">Requirement</span></span> | <span data-ttu-id="bf25a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf25a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf25a-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf25a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bf25a-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf25a-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="bf25a-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf25a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bf25a-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bf25a-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="bf25a-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bf25a-121">Namespace</span></span><br/>                | <span data-ttu-id="bf25a-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="bf25a-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="bf25a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf25a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf25a-124"><dt>Certenroll. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf25a-124"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="bf25a-125">MOF</span><span class="sxs-lookup"><span data-stu-id="bf25a-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf25a-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf25a-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf25a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="bf25a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf25a-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf25a-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="bf25a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf25a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf25a-130">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="bf25a-130">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





