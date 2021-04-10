---
title: Méthode GetSecondaryConnectionString de la classe Win32_RDMSDeploymentSettings
description: Récupère la chaîne de connexion secondaire de la base de données au niveau du déploiement, qui peut être utilisée pour prendre en charge l’expiration du mot de passe.
ms.assetid: 0de02752-6cbf-4c21-b752-a57ed58aeef1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetSecondaryConnectionString
- Services Bureau à distance de la méthode GetSecondaryConnectionString, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode GetSecondaryConnectionString
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetSecondaryConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2c09f4fcacabbe928fcda00447e252077bd8a51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317233"
---
# <a name="getsecondaryconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="5b846-106">Méthode GetSecondaryConnectionString de la \_ classe Win32 RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="5b846-106">GetSecondaryConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="5b846-107">Récupère la chaîne de connexion secondaire de la base de données au niveau du déploiement, qui peut être utilisée pour prendre en charge l’expiration du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="5b846-107">Retrieves the deployment-level database secondary connection string, which may be used to support password expiration.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b846-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b846-108">Syntax</span></span>


```mof
uint32 GetSecondaryConnectionString(
  [out] string SecondaryConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="5b846-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b846-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b846-110">*SecondaryConnectionString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5b846-110">*SecondaryConnectionString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b846-111">Chaîne de connexion à récupérer</span><span class="sxs-lookup"><span data-stu-id="5b846-111">The connection string to retrieve</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b846-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5b846-112">Return value</span></span>

<span data-ttu-id="5b846-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="5b846-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b846-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b846-114">Requirements</span></span>



| <span data-ttu-id="5b846-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b846-115">Requirement</span></span> | <span data-ttu-id="5b846-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b846-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b846-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b846-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5b846-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b846-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="5b846-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b846-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5b846-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5b846-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="5b846-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5b846-121">Namespace</span></span><br/>                | <span data-ttu-id="5b846-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="5b846-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="5b846-123">MOF</span><span class="sxs-lookup"><span data-stu-id="5b846-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b846-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b846-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b846-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5b846-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b846-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b846-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="5b846-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b846-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b846-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="5b846-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





