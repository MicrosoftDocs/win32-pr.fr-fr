---
title: Méthode Delete de la classe Win32_Terminal
description: Supprime le terminal spécifié.
ms.assetid: 59d8cc73-aef1-49d2-a7a2-dd3cbe5a8c52
ms.tgt_platform: multiple
keywords:
- Supprimer la méthode Services Bureau à distance
- Delete, méthode Services Bureau à distance, classe Win32_Terminal
- Win32_Terminal de la classe Services Bureau à distance, méthode Delete
topic_type:
- apiref
api_name:
- Win32_Terminal.Delete
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47b7120c78eada2b047f836219d3382e5ce1e2f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512366"
---
# <a name="delete-method-of-the-win32_terminal-class"></a><span data-ttu-id="223cb-106">Méthode Delete de la \_ classe de terminal Win32</span><span class="sxs-lookup"><span data-stu-id="223cb-106">Delete method of the Win32\_Terminal class</span></span>

<span data-ttu-id="223cb-107">La méthode **Delete** supprime le terminal spécifié.</span><span class="sxs-lookup"><span data-stu-id="223cb-107">The **Delete** method deletes the specified terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="223cb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="223cb-108">Syntax</span></span>


```mof
uint32 Delete(
  [in] string NewTerminalName
);
```



## <a name="parameters"></a><span data-ttu-id="223cb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="223cb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="223cb-110">*NewTerminalName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="223cb-110">*NewTerminalName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="223cb-111">Nom du terminal à supprimer.</span><span class="sxs-lookup"><span data-stu-id="223cb-111">Name of the terminal to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="223cb-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="223cb-112">Return value</span></span>

<span data-ttu-id="223cb-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="223cb-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="223cb-114">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="223cb-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="223cb-115">Notes</span><span class="sxs-lookup"><span data-stu-id="223cb-115">Remarks</span></span>

<span data-ttu-id="223cb-116">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="223cb-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="223cb-117">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="223cb-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="223cb-118">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="223cb-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="223cb-119">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="223cb-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="223cb-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="223cb-120">Requirements</span></span>



| <span data-ttu-id="223cb-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="223cb-121">Requirement</span></span> | <span data-ttu-id="223cb-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="223cb-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="223cb-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="223cb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="223cb-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="223cb-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="223cb-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="223cb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="223cb-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="223cb-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="223cb-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="223cb-127">Namespace</span></span><br/>                | <span data-ttu-id="223cb-128">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="223cb-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="223cb-129">MOF</span><span class="sxs-lookup"><span data-stu-id="223cb-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="223cb-130"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="223cb-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="223cb-131">DLL</span><span class="sxs-lookup"><span data-stu-id="223cb-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="223cb-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="223cb-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="223cb-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="223cb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="223cb-134">**\_Terminal Win32**</span><span class="sxs-lookup"><span data-stu-id="223cb-134">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

