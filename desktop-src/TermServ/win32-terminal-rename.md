---
title: Renommer la méthode de la classe Win32_Terminal
description: La méthode Rename renomme le terminal.
ms.assetid: 85b5c83b-8ca3-4ed0-852b-b11ba98c18a6
ms.tgt_platform: multiple
keywords:
- Renommer la méthode Services Bureau à distance
- Renommer la méthode Services Bureau à distance, classe Win32_Terminal
- Win32_Terminal de la classe Services Bureau à distance, renommer la méthode
topic_type:
- apiref
api_name:
- Win32_Terminal.Rename
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0258277bd509f7f72d5e314bc20d9852fa03315a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513584"
---
# <a name="rename-method-of-the-win32_terminal-class"></a><span data-ttu-id="da3d1-106">Renommer la méthode de la \_ classe de terminal Win32</span><span class="sxs-lookup"><span data-stu-id="da3d1-106">Rename method of the Win32\_Terminal class</span></span>

<span data-ttu-id="da3d1-107">La méthode **Rename** renomme le terminal.</span><span class="sxs-lookup"><span data-stu-id="da3d1-107">The **Rename** method renames the terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="da3d1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da3d1-108">Syntax</span></span>


```mof
uint32 Rename(
  [in] string NewTerminalName
);
```



## <a name="parameters"></a><span data-ttu-id="da3d1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da3d1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da3d1-110">*NewTerminalName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da3d1-110">*NewTerminalName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da3d1-111">Nouveau nom du terminal.</span><span class="sxs-lookup"><span data-stu-id="da3d1-111">The new name of the terminal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da3d1-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="da3d1-112">Return value</span></span>

<span data-ttu-id="da3d1-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="da3d1-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="da3d1-114">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="da3d1-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="da3d1-115">Notes</span><span class="sxs-lookup"><span data-stu-id="da3d1-115">Remarks</span></span>

<span data-ttu-id="da3d1-116">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="da3d1-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="da3d1-117">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="da3d1-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="da3d1-118">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="da3d1-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="da3d1-119">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="da3d1-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="da3d1-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da3d1-120">Requirements</span></span>



| <span data-ttu-id="da3d1-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da3d1-121">Requirement</span></span> | <span data-ttu-id="da3d1-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="da3d1-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da3d1-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da3d1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="da3d1-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da3d1-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da3d1-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da3d1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="da3d1-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da3d1-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da3d1-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="da3d1-127">Namespace</span></span><br/>                | <span data-ttu-id="da3d1-128">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="da3d1-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="da3d1-129">MOF</span><span class="sxs-lookup"><span data-stu-id="da3d1-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da3d1-130"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da3d1-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="da3d1-131">DLL</span><span class="sxs-lookup"><span data-stu-id="da3d1-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da3d1-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da3d1-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da3d1-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da3d1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da3d1-134">**\_Terminal Win32**</span><span class="sxs-lookup"><span data-stu-id="da3d1-134">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

