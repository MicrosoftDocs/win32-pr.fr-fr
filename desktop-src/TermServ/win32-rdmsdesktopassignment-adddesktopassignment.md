---
title: Méthode AddDesktopAssignment de la classe Win32_RDMSDesktopAssignment
description: Ajoutez une attribution de bureau.
ms.assetid: 3690f70e-d0c3-444a-a0b7-cec6994eb3b8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AddDesktopAssignment
- Services Bureau à distance de la méthode AddDesktopAssignment, classe Win32_RDMSDesktopAssignment
- Win32_RDMSDesktopAssignment de la classe Services Bureau à distance, méthode AddDesktopAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.AddDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 571273e76b0bb45b748f1587e5a831fcf1e36b0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843398"
---
# <a name="adddesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a><span data-ttu-id="aaa12-106">Méthode AddDesktopAssignment de la \_ classe Win32 RDMSDesktopAssignment</span><span class="sxs-lookup"><span data-stu-id="aaa12-106">AddDesktopAssignment method of the Win32\_RDMSDesktopAssignment class</span></span>

<span data-ttu-id="aaa12-107">Ajouter une attribution de bureau</span><span class="sxs-lookup"><span data-stu-id="aaa12-107">Add a desktop assignment</span></span>

## <a name="syntax"></a><span data-ttu-id="aaa12-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aaa12-108">Syntax</span></span>


```mof
uint32 AddDesktopAssignment(
  [in] string CollectionAlias,
  [in] string DesktopName,
  [in] string UserDomain,
  [in] string UserName
);
```



## <a name="parameters"></a><span data-ttu-id="aaa12-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aaa12-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaa12-110">*CollectionAlias* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aaa12-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa12-111">Alias de collection.</span><span class="sxs-lookup"><span data-stu-id="aaa12-111">The collection alias.</span></span>

</dd> <dt>

<span data-ttu-id="aaa12-112">*DesktopName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aaa12-112">*DesktopName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa12-113">Nom du bureau.</span><span class="sxs-lookup"><span data-stu-id="aaa12-113">The name of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="aaa12-114">*UserDomain* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aaa12-114">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa12-115">Nom de domaine du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="aaa12-115">The user account domain name.</span></span>

</dd> <dt>

<span data-ttu-id="aaa12-116">*Nom d’utilisateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aaa12-116">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa12-117">Nom du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="aaa12-117">The user account name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aaa12-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aaa12-118">Requirements</span></span>



| <span data-ttu-id="aaa12-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aaa12-119">Requirement</span></span> | <span data-ttu-id="aaa12-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="aaa12-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaa12-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aaa12-121">Minimum supported client</span></span><br/> | <span data-ttu-id="aaa12-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="aaa12-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="aaa12-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aaa12-123">Minimum supported server</span></span><br/> | <span data-ttu-id="aaa12-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="aaa12-124">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="aaa12-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="aaa12-125">Namespace</span></span><br/>                | <span data-ttu-id="aaa12-126">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="aaa12-126">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="aaa12-127">MOF</span><span class="sxs-lookup"><span data-stu-id="aaa12-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aaa12-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aaa12-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="aaa12-129">DLL</span><span class="sxs-lookup"><span data-stu-id="aaa12-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aaa12-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aaa12-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="aaa12-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aaa12-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaa12-132">**\_RDMSDesktopAssignment Win32**</span><span class="sxs-lookup"><span data-stu-id="aaa12-132">**Win32\_RDMSDesktopAssignment**</span></span>](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 





