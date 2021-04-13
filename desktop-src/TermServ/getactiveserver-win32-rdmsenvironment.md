---
title: Méthode GetActiveServer de la classe Win32_RDMSEnvironment
description: Récupère le nom de domaine complet (FQDN) de l’environnement Bureau à distance Management Services (RDMS).
ms.assetid: 87e25d11-de1d-41d1-974d-2871dde444b5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetActiveServer
- Services Bureau à distance de la méthode GetActiveServer, classe Win32_RDMSEnvironment
- Win32_RDMSEnvironment de la classe Services Bureau à distance, méthode GetActiveServer
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4265315e3ed2de87e564adab87c023401bbd55e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465802"
---
# <a name="getactiveserver-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="9fd90-106">Méthode GetActiveServer de la \_ classe Win32 RDMSEnvironment</span><span class="sxs-lookup"><span data-stu-id="9fd90-106">GetActiveServer method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="9fd90-107">Récupère le nom de domaine complet (FQDN) de l’environnement Bureau à distance Management Services (RDMS).</span><span class="sxs-lookup"><span data-stu-id="9fd90-107">Retrieves the fully qualified domain name (FQDN) of the Remote Desktop Management Services (RDMS) environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fd90-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9fd90-108">Syntax</span></span>


```mof
uint32 GetActiveServer(
  [out] string ServerName
);
```



## <a name="parameters"></a><span data-ttu-id="9fd90-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9fd90-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fd90-110">*Nom du serveur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9fd90-110">*ServerName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fd90-111">Reçoit le nom de domaine complet récupéré.</span><span class="sxs-lookup"><span data-stu-id="9fd90-111">Receives the retrieved FQDN.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fd90-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9fd90-112">Return value</span></span>

<span data-ttu-id="9fd90-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="9fd90-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fd90-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9fd90-114">Requirements</span></span>



| <span data-ttu-id="9fd90-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9fd90-115">Requirement</span></span> | <span data-ttu-id="9fd90-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fd90-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd90-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9fd90-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9fd90-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9fd90-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="9fd90-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9fd90-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9fd90-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9fd90-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="9fd90-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9fd90-121">Namespace</span></span><br/>                | <span data-ttu-id="9fd90-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="9fd90-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="9fd90-123">MOF</span><span class="sxs-lookup"><span data-stu-id="9fd90-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9fd90-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9fd90-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="9fd90-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9fd90-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fd90-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fd90-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="9fd90-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9fd90-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fd90-128">**\_RDMSEnvironment Win32**</span><span class="sxs-lookup"><span data-stu-id="9fd90-128">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





