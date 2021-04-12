---
title: Méthode GetUserAssignment de la classe Win32_RDMSVirtualDesktop
description: Récupère le nom d’utilisateur et le nom de domaine de l’utilisateur affecté au bureau virtuel.
ms.assetid: 1887c49d-85df-4fb4-9b40-42fb7763bf95
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetUserAssignment
- Services Bureau à distance de la méthode GetUserAssignment, classe Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop de la classe Services Bureau à distance, méthode GetUserAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87293a471bb4f69b3f4c57de0f964fa0daa043cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384900"
---
# <a name="getuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="e4b09-106">Méthode GetUserAssignment de la \_ classe Win32 RDMSVirtualDesktop</span><span class="sxs-lookup"><span data-stu-id="e4b09-106">GetUserAssignment method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="e4b09-107">Récupère le nom d’utilisateur et le nom de domaine de l’utilisateur affecté au bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="e4b09-107">Retrieves the username and domain name of the user that is assigned to the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4b09-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4b09-108">Syntax</span></span>


```mof
uint32 GetUserAssignment(
  [out] string UserName,
  [out] string UserDomain
);
```



## <a name="parameters"></a><span data-ttu-id="e4b09-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4b09-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4b09-110">*Nom d’utilisateur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e4b09-110">*UserName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4b09-111">Reçoit le nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e4b09-111">Receives the username.</span></span>

</dd> <dt>

<span data-ttu-id="e4b09-112">*UserDomain* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e4b09-112">*UserDomain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4b09-113">Reçoit le nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="e4b09-113">Receives the domain name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4b09-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e4b09-114">Return value</span></span>

<span data-ttu-id="e4b09-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="e4b09-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4b09-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4b09-116">Requirements</span></span>



| <span data-ttu-id="e4b09-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4b09-117">Requirement</span></span> | <span data-ttu-id="e4b09-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4b09-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b09-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4b09-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e4b09-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4b09-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="e4b09-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4b09-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e4b09-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e4b09-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="e4b09-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e4b09-123">Namespace</span></span><br/>                | <span data-ttu-id="e4b09-124">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="e4b09-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="e4b09-125">MOF</span><span class="sxs-lookup"><span data-stu-id="e4b09-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4b09-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4b09-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4b09-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e4b09-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4b09-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4b09-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="e4b09-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4b09-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4b09-130">**\_RDMSVirtualDesktop Win32**</span><span class="sxs-lookup"><span data-stu-id="e4b09-130">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





