---
title: Méthode DumpVmInfo de la classe Win32_TSVm
description: Ce membre est destiné à des fins de test interne et ne doit pas être utilisé dans votre code.
ms.assetid: 40cb4fdc-f657-47c6-8daa-684a12be30e4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode DumpVmInfo
- Services Bureau à distance de la méthode DumpVmInfo, classe Win32_TSVm
- Win32_TSVm de la classe Services Bureau à distance, méthode DumpVmInfo
topic_type:
- apiref
api_name:
- Win32_TSVm.DumpVmInfo
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a2d02a1d4ea07bd045da2850a4d7ccb0069977a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743845"
---
# <a name="dumpvminfo-method-of-the-win32_tsvm-class"></a><span data-ttu-id="2e47c-106">Méthode DumpVmInfo de la \_ classe Win32 TSVm</span><span class="sxs-lookup"><span data-stu-id="2e47c-106">DumpVmInfo method of the Win32\_TSVm class</span></span>

<span data-ttu-id="2e47c-107">Ce membre est destiné à des fins de test interne et ne doit pas être utilisé dans votre code.</span><span class="sxs-lookup"><span data-stu-id="2e47c-107">This member is for internal testing purposes, and should not be used in your code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e47c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e47c-108">Syntax</span></span>


```mof
uint32 DumpVmInfo();
```



## <a name="parameters"></a><span data-ttu-id="2e47c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e47c-109">Parameters</span></span>

<span data-ttu-id="2e47c-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2e47c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e47c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2e47c-111">Return value</span></span>

<span data-ttu-id="2e47c-112">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="2e47c-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="2e47c-113">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="2e47c-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e47c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e47c-114">Requirements</span></span>



| <span data-ttu-id="2e47c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e47c-115">Requirement</span></span> | <span data-ttu-id="2e47c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e47c-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e47c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e47c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2e47c-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e47c-118">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="2e47c-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e47c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2e47c-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2e47c-120">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="2e47c-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2e47c-121">Namespace</span></span><br/>                | <span data-ttu-id="2e47c-122">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="2e47c-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="2e47c-123">MOF</span><span class="sxs-lookup"><span data-stu-id="2e47c-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e47c-124"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e47c-124"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="2e47c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2e47c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e47c-126"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e47c-126"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e47c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e47c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e47c-128">**\_TSVm Win32**</span><span class="sxs-lookup"><span data-stu-id="2e47c-128">**Win32\_TSVm**</span></span>](win32-tsvm.md)
</dt> </dl>

 

 





