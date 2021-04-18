---
title: Méthode GetClientAccessName de la classe Win32_RDMSEnvironment
description: Récupère le nom de l’enregistrement de ressource (RR) du système de noms de domaine (DNS) de l’environnement des services de gestion de Bureau à distance (RDMS).
ms.assetid: 16f9d00d-a398-4a73-a641-ac552ba6a9d3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetClientAccessName
- Services Bureau à distance de la méthode GetClientAccessName, classe Win32_RDMSEnvironment
- Win32_RDMSEnvironment de la classe Services Bureau à distance, méthode GetClientAccessName
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54662cf1f27c53f3bf69398a203bfdfce1e53c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512550"
---
# <a name="getclientaccessname-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="1d5b3-106">Méthode GetClientAccessName de la \_ classe Win32 RDMSEnvironment</span><span class="sxs-lookup"><span data-stu-id="1d5b3-106">GetClientAccessName method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="1d5b3-107">Récupère le nom de l’enregistrement de ressource (RR) du système de noms de domaine (DNS) de l’environnement des services de gestion de Bureau à distance (RDMS).</span><span class="sxs-lookup"><span data-stu-id="1d5b3-107">Retrieves the Domain Name System (DNS) resource record (RR) name of the Remote Desktop Management Services (RDMS) environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d5b3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d5b3-108">Syntax</span></span>


```mof
uint32 GetClientAccessName(
  [out] string ClientAccessName
);
```



## <a name="parameters"></a><span data-ttu-id="1d5b3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d5b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d5b3-110">*ClientAccessName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1d5b3-110">*ClientAccessName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d5b3-111">Reçoit le nom de l’enregistrement de ressource récupéré.</span><span class="sxs-lookup"><span data-stu-id="1d5b3-111">Receives the retrieved RR name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d5b3-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d5b3-112">Return value</span></span>

<span data-ttu-id="1d5b3-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="1d5b3-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d5b3-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d5b3-114">Requirements</span></span>



| <span data-ttu-id="1d5b3-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d5b3-115">Requirement</span></span> | <span data-ttu-id="1d5b3-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d5b3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d5b3-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d5b3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1d5b3-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d5b3-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="1d5b3-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d5b3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1d5b3-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1d5b3-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="1d5b3-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1d5b3-121">Namespace</span></span><br/>                | <span data-ttu-id="1d5b3-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="1d5b3-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="1d5b3-123">MOF</span><span class="sxs-lookup"><span data-stu-id="1d5b3-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d5b3-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d5b3-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d5b3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1d5b3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d5b3-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d5b3-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="1d5b3-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d5b3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d5b3-128">**\_RDMSEnvironment Win32**</span><span class="sxs-lookup"><span data-stu-id="1d5b3-128">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





