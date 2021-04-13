---
title: Méthode SetProgramList de la classe Win32_TSVirtualIP
description: Remplace la liste des programmes qui utilisent la virtualisation IP.
ms.assetid: 4137c9b0-5b4d-4ab6-af2e-2cd98ba53563
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetProgramList
- Services Bureau à distance de la méthode SetProgramList, classe Win32_TSVirtualIP
- Win32_TSVirtualIP de la classe Services Bureau à distance, méthode SetProgramList
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetProgramList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f86c5d530b3393ac1be8858a7ce57ee70ab9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508738"
---
# <a name="setprogramlist-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="e95c2-106">Méthode SetProgramList de la \_ classe Win32 TSVirtualIP</span><span class="sxs-lookup"><span data-stu-id="e95c2-106">SetProgramList method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="e95c2-107">Remplace la liste des programmes qui utilisent la virtualisation IP.</span><span class="sxs-lookup"><span data-stu-id="e95c2-107">Overwrites the list of programs that use IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="e95c2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e95c2-108">Syntax</span></span>


```mof
unint32 SetProgramList(
  [in] string ProgramList[]
);
```



## <a name="parameters"></a><span data-ttu-id="e95c2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e95c2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e95c2-110">*ProgramList* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e95c2-110">*ProgramList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e95c2-111">Type : **chaîne \[ \]**</span><span class="sxs-lookup"><span data-stu-id="e95c2-111">Type: **string\[\]**</span></span>

<span data-ttu-id="e95c2-112">Tableau de chaînes qui contient le chemin d’accès et les noms de fichiers des programmes qui utilisent la virtualisation IP.</span><span class="sxs-lookup"><span data-stu-id="e95c2-112">An array of strings that contain the path and file names of the programs that use IP virtualization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e95c2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e95c2-113">Return value</span></span>

<span data-ttu-id="e95c2-114">Type : **unint32**</span><span class="sxs-lookup"><span data-stu-id="e95c2-114">Type: **unint32**</span></span>

<span data-ttu-id="e95c2-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="e95c2-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="e95c2-116">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="e95c2-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="e95c2-117">La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e95c2-117">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="e95c2-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e95c2-118">Requirements</span></span>



| <span data-ttu-id="e95c2-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e95c2-119">Requirement</span></span> | <span data-ttu-id="e95c2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e95c2-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e95c2-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e95c2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e95c2-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e95c2-122">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e95c2-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e95c2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e95c2-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e95c2-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="e95c2-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e95c2-125">Namespace</span></span><br/>                | <span data-ttu-id="e95c2-126">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="e95c2-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e95c2-127">MOF</span><span class="sxs-lookup"><span data-stu-id="e95c2-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e95c2-128"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e95c2-128"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e95c2-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e95c2-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e95c2-130"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e95c2-130"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e95c2-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e95c2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e95c2-132">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="e95c2-132">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





