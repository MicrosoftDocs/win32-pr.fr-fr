---
title: Méthode GetVirtualDesktopDetails de la classe Win32_RDMSVirtualDesktop
description: Récupère les informations supplémentaires sur le bureau virtuel.
ms.assetid: 487e3a02-4306-4639-a44e-5b9519163a67
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetVirtualDesktopDetails
- Services Bureau à distance de la méthode GetVirtualDesktopDetails, classe Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop de la classe Services Bureau à distance, méthode GetVirtualDesktopDetails
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopDetails
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7382a7ea10b3e557cd7317bdf1ddb0c4bcea55d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465794"
---
# <a name="getvirtualdesktopdetails-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="d7fe3-106">Méthode GetVirtualDesktopDetails de la \_ classe Win32 RDMSVirtualDesktop</span><span class="sxs-lookup"><span data-stu-id="d7fe3-106">GetVirtualDesktopDetails method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="d7fe3-107">Récupère les informations supplémentaires sur le bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="d7fe3-107">Retrieves the additional information about the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7fe3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7fe3-108">Syntax</span></span>


```mof
uint32 GetVirtualDesktopDetails(
  [out] uint32  RAMSizeInMB,
  [out] boolean RemoteFXEnabled,
  [out] string  OSVersion
);
```



## <a name="parameters"></a><span data-ttu-id="d7fe3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7fe3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7fe3-110">*RAMSizeInMB* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d7fe3-110">*RAMSizeInMB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7fe3-111">Reçoit la quantité de mémoire vive (RAM) affectée au bureau virtuel, en octets.</span><span class="sxs-lookup"><span data-stu-id="d7fe3-111">Receives the amount of RAM assigned to the virtual desktop, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d7fe3-112">*RemoteFXEnabled* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d7fe3-112">*RemoteFXEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7fe3-113">Reçoit une valeur qui indique si RemoteFX est activé sur le bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="d7fe3-113">Receives a value that indicates whether RemoteFX is enabled on the virtual desktop.</span></span> <span data-ttu-id="d7fe3-114">**True** si RemoteFX est activé ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="d7fe3-114">**TRUE** if RemoteFX is enabled; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d7fe3-115">*OSVersion* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d7fe3-115">*OSVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7fe3-116">Reçoit la version du système d’exploitation du bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="d7fe3-116">Receives the OS version of the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7fe3-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d7fe3-117">Return value</span></span>

<span data-ttu-id="d7fe3-118">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="d7fe3-118">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7fe3-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7fe3-119">Requirements</span></span>



| <span data-ttu-id="d7fe3-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7fe3-120">Requirement</span></span> | <span data-ttu-id="d7fe3-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7fe3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7fe3-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7fe3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d7fe3-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7fe3-123">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="d7fe3-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7fe3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d7fe3-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d7fe3-125">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="d7fe3-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d7fe3-126">Namespace</span></span><br/>                | <span data-ttu-id="d7fe3-127">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="d7fe3-127">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="d7fe3-128">MOF</span><span class="sxs-lookup"><span data-stu-id="d7fe3-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7fe3-129"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7fe3-129"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7fe3-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d7fe3-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7fe3-131"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7fe3-131"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="d7fe3-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7fe3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7fe3-133">**\_RDMSVirtualDesktop Win32**</span><span class="sxs-lookup"><span data-stu-id="d7fe3-133">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





