---
title: Méthode RemoveVirtualDesktop de la classe Win32_RDMSVirtualDesktopCollection
description: Supprime un bureau virtuel de la collection de bureaux virtuels.
ms.assetid: 287ebbb2-86db-4b4a-8dbb-ac5472789e72
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RemoveVirtualDesktop
- Services Bureau à distance de la méthode RemoveVirtualDesktop, classe Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de la classe Services Bureau à distance, méthode RemoveVirtualDesktop
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.RemoveVirtualDesktop
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a468de22d571fa52d37c2ad51d40d492af35384a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508409"
---
# <a name="removevirtualdesktop-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="08303-106">Méthode RemoveVirtualDesktop de la \_ classe Win32 RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="08303-106">RemoveVirtualDesktop method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="08303-107">Supprime un bureau virtuel de la collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="08303-107">Removes a virtual desktop from the virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="08303-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08303-108">Syntax</span></span>


```mof
uint32 RemoveVirtualDesktop(
  [in] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="08303-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08303-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08303-110">*Vmname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="08303-110">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08303-111">Nom de la machine virtuelle qui héberge le bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="08303-111">The name of the virtual machine that hosts the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08303-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="08303-112">Return value</span></span>

<span data-ttu-id="08303-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="08303-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="08303-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08303-114">Requirements</span></span>



| <span data-ttu-id="08303-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08303-115">Requirement</span></span> | <span data-ttu-id="08303-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="08303-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="08303-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08303-117">Minimum supported client</span></span><br/> | <span data-ttu-id="08303-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="08303-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="08303-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08303-119">Minimum supported server</span></span><br/> | <span data-ttu-id="08303-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="08303-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="08303-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="08303-121">Namespace</span></span><br/>                | <span data-ttu-id="08303-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="08303-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="08303-123">MOF</span><span class="sxs-lookup"><span data-stu-id="08303-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08303-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08303-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="08303-125">DLL</span><span class="sxs-lookup"><span data-stu-id="08303-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08303-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08303-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="08303-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08303-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08303-128">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="08303-128">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





