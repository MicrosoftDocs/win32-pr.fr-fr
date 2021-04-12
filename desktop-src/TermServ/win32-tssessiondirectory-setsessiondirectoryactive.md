---
title: Méthode SetSessionDirectoryActive de la classe Win32_TSSessionDirectory
description: La méthode SetSessionDirectoryActive définit la propriété SessionDirectoryActive.
ms.assetid: b2175d1a-b62f-4bdf-9122-76e85233fba4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetSessionDirectoryActive
- Services Bureau à distance de la méthode SetSessionDirectoryActive, classe Win32_TSSessionDirectory
- Win32_TSSessionDirectory de la classe Services Bureau à distance, méthode SetSessionDirectoryActive
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca8709028ee90db549c7cdeb053b04dc88b52ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384440"
---
# <a name="setsessiondirectoryactive-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="8d5d5-106">Méthode SetSessionDirectoryActive de la \_ classe Win32 TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="8d5d5-106">SetSessionDirectoryActive method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="8d5d5-107">La méthode **SetSessionDirectoryActive** définit la propriété **SessionDirectoryActive** .</span><span class="sxs-lookup"><span data-stu-id="8d5d5-107">The **SetSessionDirectoryActive** method sets the **SessionDirectoryActive** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d5d5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d5d5-108">Syntax</span></span>


```mof
uint32 SetSessionDirectoryActive(
  [in] uint32 SessionDirectoryActive
);
```



## <a name="parameters"></a><span data-ttu-id="8d5d5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d5d5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d5d5-110">*SessionDirectoryActive* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d5d5-110">*SessionDirectoryActive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d5d5-111">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d5d5-111">Type: **uint32**</span></span>

<span data-ttu-id="8d5d5-112">Indicateur de désactivation ou d’activation du service d’annuaire de sessions.</span><span class="sxs-lookup"><span data-stu-id="8d5d5-112">Flag disabling or enabling the Session Directory service.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="8d5d5-113"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="8d5d5-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="8d5d5-114">Désactivez le service d’annuaire de sessions.</span><span class="sxs-lookup"><span data-stu-id="8d5d5-114">Disable the Session Directory service.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="8d5d5-115"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="8d5d5-115"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="8d5d5-116">Activez le service d’annuaire de sessions.</span><span class="sxs-lookup"><span data-stu-id="8d5d5-116">Enable the Session Directory service.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d5d5-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8d5d5-117">Return value</span></span>

<span data-ttu-id="8d5d5-118">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d5d5-118">Type: **uint32**</span></span>

<span data-ttu-id="8d5d5-119">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="8d5d5-119">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="8d5d5-120">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="8d5d5-120">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="8d5d5-121">La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8d5d5-121">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d5d5-122">Notes</span><span class="sxs-lookup"><span data-stu-id="8d5d5-122">Remarks</span></span>

<span data-ttu-id="8d5d5-123">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="8d5d5-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8d5d5-124">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8d5d5-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8d5d5-125">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="8d5d5-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8d5d5-126">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8d5d5-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d5d5-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d5d5-127">Requirements</span></span>



| <span data-ttu-id="8d5d5-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d5d5-128">Requirement</span></span> | <span data-ttu-id="8d5d5-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d5d5-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d5d5-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d5d5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8d5d5-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d5d5-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="8d5d5-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d5d5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8d5d5-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d5d5-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8d5d5-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8d5d5-134">Namespace</span></span><br/>                | <span data-ttu-id="8d5d5-135">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="8d5d5-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8d5d5-136">MOF</span><span class="sxs-lookup"><span data-stu-id="8d5d5-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d5d5-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d5d5-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d5d5-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8d5d5-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d5d5-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d5d5-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d5d5-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d5d5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d5d5-141">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="8d5d5-141">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

