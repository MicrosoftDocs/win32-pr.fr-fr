---
title: Méthode Export de la classe Win32_TSVm
description: Récupère les informations de surveillance de session de l’ordinateur virtuel.
ms.assetid: 7996651c-aa7c-4fde-84a6-928b27c8c5b8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode d’exportation
- Méthode d’exportation Services Bureau à distance, classe Win32_TSVm
- Services Bureau à distance de la classe Win32_TSVm, méthode d’exportation
topic_type:
- apiref
api_name:
- Win32_TSVm.Export
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d94b24af5563f9cdb668e269c260e8fe19049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511933"
---
# <a name="export-method-of-the-win32_tsvm-class"></a><span data-ttu-id="22021-106">Méthode Export de la \_ classe TSVm Win32</span><span class="sxs-lookup"><span data-stu-id="22021-106">Export method of the Win32\_TSVm class</span></span>

<span data-ttu-id="22021-107">Récupère les informations de surveillance de session de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="22021-107">Retrieves the virtual machine session monitoring information.</span></span>

## <a name="syntax"></a><span data-ttu-id="22021-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22021-108">Syntax</span></span>


```mof
uint32 Export(
  [in]  string ExportFolderPath,
  [out] string ExportJobObjectPath
);
```



## <a name="parameters"></a><span data-ttu-id="22021-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22021-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22021-110">*ExportFolderPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="22021-110">*ExportFolderPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22021-111">Chemin d’accès à l’emplacement où l’ordinateur virtuel sera exporté.</span><span class="sxs-lookup"><span data-stu-id="22021-111">Path to where the virtual machine will be exported.</span></span>

</dd> <dt>

<span data-ttu-id="22021-112">*ExportJobObjectPath* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="22021-112">*ExportJobObjectPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22021-113">En cas de réussite, retourne le chemin d’accès de l’objet ConcreteJob HyperV.</span><span class="sxs-lookup"><span data-stu-id="22021-113">On a success returns the HyperV ConcreteJob object path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22021-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22021-114">Return value</span></span>

<span data-ttu-id="22021-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="22021-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="22021-116">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="22021-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="22021-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22021-117">Requirements</span></span>



| <span data-ttu-id="22021-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22021-118">Requirement</span></span> | <span data-ttu-id="22021-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="22021-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="22021-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22021-120">Minimum supported client</span></span><br/> | <span data-ttu-id="22021-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="22021-121">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="22021-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22021-122">Minimum supported server</span></span><br/> | <span data-ttu-id="22021-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="22021-123">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="22021-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="22021-124">Namespace</span></span><br/>                | <span data-ttu-id="22021-125">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="22021-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="22021-126">MOF</span><span class="sxs-lookup"><span data-stu-id="22021-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22021-127"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="22021-127"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="22021-128">DLL</span><span class="sxs-lookup"><span data-stu-id="22021-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22021-129"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22021-129"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22021-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22021-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22021-131">**\_TSVm Win32**</span><span class="sxs-lookup"><span data-stu-id="22021-131">**Win32\_TSVm**</span></span>](win32-tsvm.md)
</dt> </dl>

 

 





