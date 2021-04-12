---
title: Méthode SetConnectionString de la classe Win32_RDMSDeploymentSettings
description: Définit la chaîne de connexion de la base de données au niveau du déploiement.
ms.assetid: c8902ab9-72a6-4d69-ab22-f6074205deb4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetConnectionString
- Services Bureau à distance de la méthode SetConnectionString, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode SetConnectionString
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ccb3f618f6a08dcb95bb7dc04c1494be6a7b5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384447"
---
# <a name="setconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="0f3c9-106">Méthode SetConnectionString de la \_ classe Win32 RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="0f3c9-106">SetConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="0f3c9-107">Définit la chaîne de connexion de la base de données au niveau du déploiement.</span><span class="sxs-lookup"><span data-stu-id="0f3c9-107">Sets the deployment-level database connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f3c9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f3c9-108">Syntax</span></span>


```mof
uint32 SetConnectionString(
  [in] string ConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="0f3c9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f3c9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f3c9-110">*ConnectionString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0f3c9-110">*ConnectionString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f3c9-111">Chaîne de connexion à définir</span><span class="sxs-lookup"><span data-stu-id="0f3c9-111">The connection string to set</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f3c9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f3c9-112">Return value</span></span>

<span data-ttu-id="0f3c9-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="0f3c9-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f3c9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f3c9-114">Requirements</span></span>



| <span data-ttu-id="0f3c9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f3c9-115">Requirement</span></span> | <span data-ttu-id="0f3c9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f3c9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f3c9-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f3c9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0f3c9-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f3c9-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="0f3c9-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f3c9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0f3c9-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0f3c9-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="0f3c9-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0f3c9-121">Namespace</span></span><br/>                | <span data-ttu-id="0f3c9-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="0f3c9-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="0f3c9-123">MOF</span><span class="sxs-lookup"><span data-stu-id="0f3c9-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f3c9-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f3c9-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f3c9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0f3c9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f3c9-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f3c9-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="0f3c9-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f3c9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f3c9-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="0f3c9-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





