---
title: Méthode RemoveProgram de la classe Win32_TSVirtualIP (Bdaiface. h)
description: Supprime un programme de la liste des programmes qui utilisent la virtualisation IP.
ms.assetid: 2a8069a0-2c48-40d3-a850-0cdfce4fbc82
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RemoveProgram
- Services Bureau à distance de la méthode RemoveProgram, classe Win32_TSVirtualIP
- Win32_TSVirtualIP de la classe Services Bureau à distance, méthode RemoveProgram
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.RemoveProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6241664b6e56c3d387673b6a1cc50e43b413336
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743628"
---
# <a name="removeprogram-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="1da90-106">Méthode RemoveProgram de la \_ classe Win32 TSVirtualIP</span><span class="sxs-lookup"><span data-stu-id="1da90-106">RemoveProgram method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="1da90-107">Supprime un programme de la liste des programmes qui utilisent la virtualisation IP.</span><span class="sxs-lookup"><span data-stu-id="1da90-107">Removes a program from the list of programs that use IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="1da90-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1da90-108">Syntax</span></span>


```mof
uint32 RemoveProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a><span data-ttu-id="1da90-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1da90-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1da90-110">*ProgramPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1da90-110">*ProgramPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1da90-111">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1da90-111">Type: **string**</span></span>

<span data-ttu-id="1da90-112">Chemin d’accès et nom de fichier du programme à supprimer de la liste.</span><span class="sxs-lookup"><span data-stu-id="1da90-112">The path and file name of the program to remove from the list.</span></span> <span data-ttu-id="1da90-113">Si le programme est introuvable, une erreur est retournée.</span><span class="sxs-lookup"><span data-stu-id="1da90-113">If the program is not found, an error is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1da90-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1da90-114">Return value</span></span>

<span data-ttu-id="1da90-115">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1da90-115">Type: **uint32**</span></span>

<span data-ttu-id="1da90-116">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="1da90-116">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="1da90-117">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="1da90-117">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="1da90-118">La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="1da90-118">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="1da90-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1da90-119">Requirements</span></span>



| <span data-ttu-id="1da90-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1da90-120">Requirement</span></span> | <span data-ttu-id="1da90-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="1da90-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1da90-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1da90-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1da90-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1da90-123">None supported</span></span><br/>                                                               |
| <span data-ttu-id="1da90-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1da90-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1da90-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1da90-125">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="1da90-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1da90-126">Namespace</span></span><br/>                | <span data-ttu-id="1da90-127">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="1da90-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1da90-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="1da90-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1da90-129"><dt>Bdaiface. h</dt></span><span class="sxs-lookup"><span data-stu-id="1da90-129"><dt>Bdaiface.h</dt></span></span> </dl>   |
| <span data-ttu-id="1da90-130">MOF</span><span class="sxs-lookup"><span data-stu-id="1da90-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1da90-131"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1da90-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1da90-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1da90-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1da90-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1da90-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1da90-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1da90-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1da90-135">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="1da90-135">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





