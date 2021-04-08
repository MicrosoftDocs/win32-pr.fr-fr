---
title: Méthode AddProgram de la classe Win32_TSVirtualIP (Bdaiface. h)
description: Ajoute un programme à la liste des programmes qui utilisent la virtualisation IP.
ms.assetid: 4d142774-fa7a-4cfb-9305-5a61b0ef5438
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AddProgram
- Services Bureau à distance de la méthode AddProgram, classe Win32_TSVirtualIP
- Win32_TSVirtualIP de la classe Services Bureau à distance, méthode AddProgram
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.AddProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4de573e8d04500917ed44d5a0453005b3aa691bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740765"
---
# <a name="addprogram-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="45b47-106">Méthode AddProgram de la \_ classe Win32 TSVirtualIP</span><span class="sxs-lookup"><span data-stu-id="45b47-106">AddProgram method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="45b47-107">Ajoute un programme à la liste des programmes qui utilisent la virtualisation IP.</span><span class="sxs-lookup"><span data-stu-id="45b47-107">Adds a program to the list of programs that use IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="45b47-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45b47-108">Syntax</span></span>


```mof
uint32 AddProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a><span data-ttu-id="45b47-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45b47-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45b47-110">*ProgramPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="45b47-110">*ProgramPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45b47-111">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45b47-111">Type: **string**</span></span>

<span data-ttu-id="45b47-112">Chemin d’accès et nom de fichier du programme à ajouter à la liste.</span><span class="sxs-lookup"><span data-stu-id="45b47-112">The path and file name of the program to add to the list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45b47-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="45b47-113">Return value</span></span>

<span data-ttu-id="45b47-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45b47-114">Type: **uint32**</span></span>

<span data-ttu-id="45b47-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="45b47-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="45b47-116">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="45b47-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="45b47-117">La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="45b47-117">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="45b47-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45b47-118">Requirements</span></span>



| <span data-ttu-id="45b47-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45b47-119">Requirement</span></span> | <span data-ttu-id="45b47-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="45b47-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45b47-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45b47-121">Minimum supported client</span></span><br/> | <span data-ttu-id="45b47-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="45b47-122">None supported</span></span><br/>                                                               |
| <span data-ttu-id="45b47-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45b47-123">Minimum supported server</span></span><br/> | <span data-ttu-id="45b47-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="45b47-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="45b47-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="45b47-125">Namespace</span></span><br/>                | <span data-ttu-id="45b47-126">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="45b47-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="45b47-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="45b47-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="45b47-128"><dt>Bdaiface. h</dt></span><span class="sxs-lookup"><span data-stu-id="45b47-128"><dt>Bdaiface.h</dt></span></span> </dl>   |
| <span data-ttu-id="45b47-129">MOF</span><span class="sxs-lookup"><span data-stu-id="45b47-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45b47-130"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45b47-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="45b47-131">DLL</span><span class="sxs-lookup"><span data-stu-id="45b47-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45b47-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45b47-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45b47-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45b47-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45b47-134">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="45b47-134">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





