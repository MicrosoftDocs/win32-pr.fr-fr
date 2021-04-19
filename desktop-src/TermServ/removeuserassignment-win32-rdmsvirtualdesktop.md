---
title: Méthode RemoveUserAssignment de la classe Win32_RDMSVirtualDesktop
description: Supprime l’affectation d’utilisateur du bureau virtuel.
ms.assetid: 7ebb34b4-94f6-4a00-87a9-44ad28d103cb
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RemoveUserAssignment
- Services Bureau à distance de la méthode RemoveUserAssignment, classe Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop de la classe Services Bureau à distance, méthode RemoveUserAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.RemoveUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01675c777603f0eab2d22c0136b1ef6cc3522b7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509725"
---
# <a name="removeuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="124a1-106">Méthode RemoveUserAssignment de la \_ classe Win32 RDMSVirtualDesktop</span><span class="sxs-lookup"><span data-stu-id="124a1-106">RemoveUserAssignment method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="124a1-107">Supprime l’affectation d’utilisateur du bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="124a1-107">Removes the user assignment from the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="124a1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="124a1-108">Syntax</span></span>


```mof
uint32 RemoveUserAssignment(
  [in] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="124a1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="124a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="124a1-110">*Vmname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="124a1-110">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="124a1-111">Nom de la machine virtuelle du bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="124a1-111">The virtual machine name of the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="124a1-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="124a1-112">Return value</span></span>

<span data-ttu-id="124a1-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="124a1-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="124a1-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="124a1-114">Requirements</span></span>



| <span data-ttu-id="124a1-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="124a1-115">Requirement</span></span> | <span data-ttu-id="124a1-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="124a1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="124a1-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="124a1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="124a1-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="124a1-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="124a1-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="124a1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="124a1-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="124a1-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="124a1-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="124a1-121">Namespace</span></span><br/>                | <span data-ttu-id="124a1-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="124a1-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="124a1-123">MOF</span><span class="sxs-lookup"><span data-stu-id="124a1-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="124a1-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="124a1-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="124a1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="124a1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="124a1-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="124a1-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="124a1-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="124a1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="124a1-128">**\_RDMSVirtualDesktop Win32**</span><span class="sxs-lookup"><span data-stu-id="124a1-128">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





