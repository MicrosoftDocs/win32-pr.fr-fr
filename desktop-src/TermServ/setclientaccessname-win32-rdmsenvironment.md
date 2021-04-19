---
title: Méthode SetClientAccessName de la classe Win32_RDMSEnvironment
description: Met à jour le nom de l’enregistrement de ressource DNS (Domain Name System) d’un environnement Bureau à distance Management Services (RDMS).
ms.assetid: bbce3fc1-d2c5-4874-bdd0-be27fb5981d1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetClientAccessName
- Services Bureau à distance de la méthode SetClientAccessName, classe Win32_RDMSEnvironment
- Win32_RDMSEnvironment de la classe Services Bureau à distance, méthode SetClientAccessName
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13f9087fe2c2139833baeb21bc62da508c6e5989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511182"
---
# <a name="setclientaccessname-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="f2813-106">Méthode SetClientAccessName de la \_ classe Win32 RDMSEnvironment</span><span class="sxs-lookup"><span data-stu-id="f2813-106">SetClientAccessName method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="f2813-107">Met à jour le nom de l’enregistrement de ressource DNS (Domain Name System) d’un environnement Bureau à distance Management Services (RDMS).</span><span class="sxs-lookup"><span data-stu-id="f2813-107">Updates the Domain Name System (DNS) resource record (RR) name of an Remote Desktop Management Services (RDMS) environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2813-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2813-108">Syntax</span></span>


```mof
uint32 SetClientAccessName(
  [in] string ClientAccessName
);
```



## <a name="parameters"></a><span data-ttu-id="f2813-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2813-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2813-110">*ClientAccessName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2813-110">*ClientAccessName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2813-111">Nouveau nom du RR.</span><span class="sxs-lookup"><span data-stu-id="f2813-111">The new RR name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2813-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2813-112">Return value</span></span>

<span data-ttu-id="f2813-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="f2813-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2813-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2813-114">Requirements</span></span>



| <span data-ttu-id="f2813-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2813-115">Requirement</span></span> | <span data-ttu-id="f2813-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2813-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2813-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2813-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f2813-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2813-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="f2813-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2813-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f2813-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f2813-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="f2813-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f2813-121">Namespace</span></span><br/>                | <span data-ttu-id="f2813-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="f2813-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="f2813-123">MOF</span><span class="sxs-lookup"><span data-stu-id="f2813-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2813-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2813-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2813-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f2813-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2813-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2813-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="f2813-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2813-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2813-128">**\_RDMSEnvironment Win32**</span><span class="sxs-lookup"><span data-stu-id="f2813-128">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





