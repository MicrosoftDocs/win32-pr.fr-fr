---
title: Méthode SetUserAssignment de la classe Win32_RDMSVirtualDesktop
description: Affecte un bureau virtuel à un utilisateur.
ms.assetid: 6a96ccb7-5d3d-4164-a0a3-286a700b414c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetUserAssignment
- Services Bureau à distance de la méthode SetUserAssignment, classe Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop de la classe Services Bureau à distance, méthode SetUserAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.SetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f02e1cc935e344edd6a9c52016052e082e08d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509941"
---
# <a name="setuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="2b5c4-106">Méthode SetUserAssignment de la \_ classe Win32 RDMSVirtualDesktop</span><span class="sxs-lookup"><span data-stu-id="2b5c4-106">SetUserAssignment method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="2b5c4-107">Affecte un bureau virtuel à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2b5c4-107">Assigns a virtual desktop to a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b5c4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b5c4-108">Syntax</span></span>


```mof
uint32 SetUserAssignment(
  [in] string UserName,
  [in] string UserDomain
);
```



## <a name="parameters"></a><span data-ttu-id="2b5c4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b5c4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b5c4-110">*Nom d’utilisateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2b5c4-110">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b5c4-111">Nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2b5c4-111">The username of the user.</span></span>

</dd> <dt>

<span data-ttu-id="2b5c4-112">*UserDomain* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2b5c4-112">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b5c4-113">Nom de domaine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2b5c4-113">The domain name of the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b5c4-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2b5c4-114">Return value</span></span>

<span data-ttu-id="2b5c4-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="2b5c4-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b5c4-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b5c4-116">Requirements</span></span>



| <span data-ttu-id="2b5c4-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b5c4-117">Requirement</span></span> | <span data-ttu-id="2b5c4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b5c4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b5c4-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b5c4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2b5c4-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b5c4-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="2b5c4-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b5c4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2b5c4-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2b5c4-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="2b5c4-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2b5c4-123">Namespace</span></span><br/>                | <span data-ttu-id="2b5c4-124">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="2b5c4-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="2b5c4-125">MOF</span><span class="sxs-lookup"><span data-stu-id="2b5c4-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b5c4-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b5c4-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b5c4-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2b5c4-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b5c4-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b5c4-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="2b5c4-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b5c4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b5c4-130">**\_RDMSVirtualDesktop Win32**</span><span class="sxs-lookup"><span data-stu-id="2b5c4-130">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





