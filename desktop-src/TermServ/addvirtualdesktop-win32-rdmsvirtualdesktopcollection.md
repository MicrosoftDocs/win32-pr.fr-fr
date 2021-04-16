---
title: Méthode AddVirtualDesktop de la classe Win32_RDMSVirtualDesktopCollection
description: Ajoute un bureau virtuel à la collection de bureaux virtuels.
ms.assetid: 31a3aa28-6e5d-4f8a-81ff-ab011f568b6a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AddVirtualDesktop
- Services Bureau à distance de la méthode AddVirtualDesktop, classe Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de la classe Services Bureau à distance, méthode AddVirtualDesktop
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.AddVirtualDesktop
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4858f99f2ea4793fe0d83d06a0aaa429b7aa8f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508389"
---
# <a name="addvirtualdesktop-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="6ea25-106">Méthode AddVirtualDesktop de la \_ classe Win32 RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="6ea25-106">AddVirtualDesktop method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="6ea25-107">Ajoute un bureau virtuel à la collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="6ea25-107">Adds a virtual desktop to the virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ea25-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ea25-108">Syntax</span></span>


```mof
uint32 AddVirtualDesktop(
  [in] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="6ea25-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ea25-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ea25-110">*Vmname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6ea25-110">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ea25-111">Nom de la machine virtuelle qui héberge le bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="6ea25-111">The name of the virtual machine that hosts the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ea25-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6ea25-112">Return value</span></span>

<span data-ttu-id="6ea25-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="6ea25-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ea25-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ea25-114">Requirements</span></span>



| <span data-ttu-id="6ea25-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ea25-115">Requirement</span></span> | <span data-ttu-id="6ea25-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ea25-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ea25-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ea25-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6ea25-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ea25-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="6ea25-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ea25-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6ea25-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6ea25-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="6ea25-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6ea25-121">Namespace</span></span><br/>                | <span data-ttu-id="6ea25-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="6ea25-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="6ea25-123">MOF</span><span class="sxs-lookup"><span data-stu-id="6ea25-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ea25-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ea25-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ea25-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6ea25-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ea25-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ea25-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="6ea25-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ea25-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ea25-128">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="6ea25-128">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





