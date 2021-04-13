---
title: Méthode GetConnectionString de la classe Win32_RDMSDeploymentSettings
description: Récupère la chaîne de connexion de base de données au niveau du déploiement.
ms.assetid: 91a90883-9b87-42e5-af52-90226f0344bf
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetConnectionString
- Services Bureau à distance de la méthode GetConnectionString, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode GetConnectionString
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6476c938f62e0cd0e1f9d034c89fded50994946
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465551"
---
# <a name="getconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="ad2b9-106">Méthode GetConnectionString de la \_ classe Win32 RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="ad2b9-106">GetConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="ad2b9-107">Récupère la chaîne de connexion de base de données au niveau du déploiement.</span><span class="sxs-lookup"><span data-stu-id="ad2b9-107">Retrieves the deployment-level database connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad2b9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad2b9-108">Syntax</span></span>


```mof
uint32 GetConnectionString(
  [out] string ConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="ad2b9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad2b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad2b9-110">*ConnectionString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ad2b9-110">*ConnectionString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad2b9-111">Chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="ad2b9-111">The connection string</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad2b9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ad2b9-112">Return value</span></span>

<span data-ttu-id="ad2b9-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="ad2b9-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad2b9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad2b9-114">Requirements</span></span>



| <span data-ttu-id="ad2b9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad2b9-115">Requirement</span></span> | <span data-ttu-id="ad2b9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad2b9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad2b9-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad2b9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ad2b9-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad2b9-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="ad2b9-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad2b9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ad2b9-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ad2b9-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="ad2b9-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ad2b9-121">Namespace</span></span><br/>                | <span data-ttu-id="ad2b9-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="ad2b9-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="ad2b9-123">MOF</span><span class="sxs-lookup"><span data-stu-id="ad2b9-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad2b9-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad2b9-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad2b9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ad2b9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad2b9-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad2b9-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="ad2b9-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad2b9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad2b9-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="ad2b9-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





