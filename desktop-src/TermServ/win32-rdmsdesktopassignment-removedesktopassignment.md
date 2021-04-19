---
title: Méthode RemoveDesktopAssignment de la classe Win32_RDMSDesktopAssignment
description: Supprime une attribution de bureau.
ms.assetid: e1a8cf03-1d21-4bf4-a868-3da4d5bbf43b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RemoveDesktopAssignment
- Services Bureau à distance de la méthode RemoveDesktopAssignment, classe Win32_RDMSDesktopAssignment
- Win32_RDMSDesktopAssignment de la classe Services Bureau à distance, méthode RemoveDesktopAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.RemoveDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6645a79efc970cf7c3288d0765e9aac8cac68a89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513830"
---
# <a name="removedesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a><span data-ttu-id="fd6b4-106">Méthode RemoveDesktopAssignment de la \_ classe Win32 RDMSDesktopAssignment</span><span class="sxs-lookup"><span data-stu-id="fd6b4-106">RemoveDesktopAssignment method of the Win32\_RDMSDesktopAssignment class</span></span>

<span data-ttu-id="fd6b4-107">Supprime une attribution de bureau.</span><span class="sxs-lookup"><span data-stu-id="fd6b4-107">Removes a desktop assignment</span></span>

## <a name="syntax"></a><span data-ttu-id="fd6b4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd6b4-108">Syntax</span></span>


```mof
uint32 RemoveDesktopAssignment(
  [in] string CollectionAlias,
  [in] string DesktopName,
  [in] string UserDomain,
  [in] string UserName
);
```



## <a name="parameters"></a><span data-ttu-id="fd6b4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd6b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd6b4-110">*CollectionAlias* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd6b4-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6b4-111">Alias de collection.</span><span class="sxs-lookup"><span data-stu-id="fd6b4-111">The collection alias.</span></span>

</dd> <dt>

<span data-ttu-id="fd6b4-112">*DesktopName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd6b4-112">*DesktopName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6b4-113">Nom du bureau.</span><span class="sxs-lookup"><span data-stu-id="fd6b4-113">The name of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="fd6b4-114">*UserDomain* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd6b4-114">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6b4-115">Nom de domaine du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd6b4-115">The user account domain name.</span></span>

</dd> <dt>

<span data-ttu-id="fd6b4-116">*Nom d’utilisateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd6b4-116">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6b4-117">Nom du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd6b4-117">The user account name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd6b4-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd6b4-118">Requirements</span></span>



| <span data-ttu-id="fd6b4-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd6b4-119">Requirement</span></span> | <span data-ttu-id="fd6b4-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd6b4-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd6b4-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd6b4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fd6b4-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd6b4-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="fd6b4-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd6b4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fd6b4-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fd6b4-124">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="fd6b4-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fd6b4-125">Namespace</span></span><br/>                | <span data-ttu-id="fd6b4-126">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="fd6b4-126">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="fd6b4-127">MOF</span><span class="sxs-lookup"><span data-stu-id="fd6b4-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd6b4-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd6b4-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd6b4-129">DLL</span><span class="sxs-lookup"><span data-stu-id="fd6b4-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd6b4-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd6b4-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="fd6b4-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd6b4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd6b4-132">**\_RDMSDesktopAssignment Win32**</span><span class="sxs-lookup"><span data-stu-id="fd6b4-132">**Win32\_RDMSDesktopAssignment**</span></span>](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 





