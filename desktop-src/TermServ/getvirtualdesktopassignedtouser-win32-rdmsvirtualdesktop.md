---
title: Méthode GetVirtualDesktopAssignedToUser de la classe Win32_RDMSVirtualDesktop
description: Récupère le bureau virtuel affecté à l’utilisateur spécifié.
ms.assetid: cbc22c45-4492-4651-b164-a6fd717c5ab4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetVirtualDesktopAssignedToUser
- Services Bureau à distance de la méthode GetVirtualDesktopAssignedToUser, classe Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop de la classe Services Bureau à distance, méthode GetVirtualDesktopAssignedToUser
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopAssignedToUser
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcbbbed20b6b571e8867689ac901344af8e23b93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106532046"
---
# <a name="getvirtualdesktopassignedtouser-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="6d144-106">Méthode GetVirtualDesktopAssignedToUser de la \_ classe Win32 RDMSVirtualDesktop</span><span class="sxs-lookup"><span data-stu-id="6d144-106">GetVirtualDesktopAssignedToUser method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="6d144-107">Récupère le bureau virtuel affecté à l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="6d144-107">Retrieves the virtual desktop that is assigned to the specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d144-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d144-108">Syntax</span></span>


```mof
uint32 GetVirtualDesktopAssignedToUser(
  [in]  string CollectionAlias,
  [in]  string UserName,
  [in]  string UserDomain,
  [out] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="6d144-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d144-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d144-110">*CollectionAlias* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d144-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d144-111">Alias de la collection de bureaux virtuels qui contient le bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="6d144-111">The alias of the virtual desktop collection that contain the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="6d144-112">*Nom d’utilisateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d144-112">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d144-113">Nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6d144-113">The username of the user.</span></span>

</dd> <dt>

<span data-ttu-id="6d144-114">*UserDomain* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d144-114">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d144-115">Nom de domaine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6d144-115">The domain name of the user.</span></span>

</dd> <dt>

<span data-ttu-id="6d144-116">*Vmname* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6d144-116">*VMName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d144-117">Reçoit le nom de l’ordinateur virtuel du bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="6d144-117">Receives the virtual machine name of the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d144-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d144-118">Return value</span></span>

<span data-ttu-id="6d144-119">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="6d144-119">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d144-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d144-120">Requirements</span></span>



| <span data-ttu-id="6d144-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d144-121">Requirement</span></span> | <span data-ttu-id="6d144-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d144-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d144-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d144-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6d144-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d144-124">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="6d144-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d144-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6d144-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6d144-126">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="6d144-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6d144-127">Namespace</span></span><br/>                | <span data-ttu-id="6d144-128">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="6d144-128">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="6d144-129">MOF</span><span class="sxs-lookup"><span data-stu-id="6d144-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d144-130"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d144-130"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d144-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6d144-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d144-132"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d144-132"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="6d144-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d144-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d144-134">**\_RDMSVirtualDesktop Win32**</span><span class="sxs-lookup"><span data-stu-id="6d144-134">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





