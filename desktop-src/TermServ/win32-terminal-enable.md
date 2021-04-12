---
title: Activer la méthode de la classe Win32_Terminal
description: La méthode Enable désactive ou active le terminal.
ms.assetid: f249563b-6fa0-413c-9fc7-01dd16d5c561
ms.tgt_platform: multiple
keywords:
- Activer la méthode Services Bureau à distance
- Activer la Services Bureau à distance de méthode, classe Win32_Terminal
- Win32_Terminal de la classe Services Bureau à distance, Enable, méthode
topic_type:
- apiref
api_name:
- Win32_Terminal.Enable
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afedef572c65f249c48da850172bb9fc4d222c19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384147"
---
# <a name="enable-method-of-the-win32_terminal-class"></a><span data-ttu-id="c6b65-106">Activer la méthode de la \_ classe de terminal Win32</span><span class="sxs-lookup"><span data-stu-id="c6b65-106">Enable method of the Win32\_Terminal class</span></span>

<span data-ttu-id="c6b65-107">La méthode **Enable** désactive ou active le terminal.</span><span class="sxs-lookup"><span data-stu-id="c6b65-107">The **Enable** method disables or enables the terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6b65-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6b65-108">Syntax</span></span>


```mof
uint32 Enable(
  [in] uint32 fEnableTerminal
);
```



## <a name="parameters"></a><span data-ttu-id="c6b65-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6b65-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6b65-110">*fEnableTerminal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6b65-110">*fEnableTerminal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6b65-111">Indicateur qui désactive ou active le terminal.</span><span class="sxs-lookup"><span data-stu-id="c6b65-111">Flag that disables or enables the terminal.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="c6b65-112"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="c6b65-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="c6b65-113">Le terminal est désactivé.</span><span class="sxs-lookup"><span data-stu-id="c6b65-113">The terminal is disabled.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="c6b65-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="c6b65-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="c6b65-115">Le terminal est activé.</span><span class="sxs-lookup"><span data-stu-id="c6b65-115">The terminal is enabled.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6b65-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c6b65-116">Return value</span></span>

<span data-ttu-id="c6b65-117">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="c6b65-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="c6b65-118">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="c6b65-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6b65-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c6b65-119">Remarks</span></span>

<span data-ttu-id="c6b65-120">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="c6b65-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c6b65-121">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c6b65-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c6b65-122">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="c6b65-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c6b65-123">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c6b65-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6b65-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6b65-124">Requirements</span></span>



| <span data-ttu-id="c6b65-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6b65-125">Requirement</span></span> | <span data-ttu-id="c6b65-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6b65-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6b65-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6b65-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c6b65-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6b65-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c6b65-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6b65-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c6b65-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6b65-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c6b65-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c6b65-131">Namespace</span></span><br/>                | <span data-ttu-id="c6b65-132">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="c6b65-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c6b65-133">MOF</span><span class="sxs-lookup"><span data-stu-id="c6b65-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6b65-134"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6b65-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6b65-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c6b65-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6b65-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6b65-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6b65-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6b65-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6b65-138">**\_Terminal Win32**</span><span class="sxs-lookup"><span data-stu-id="c6b65-138">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

