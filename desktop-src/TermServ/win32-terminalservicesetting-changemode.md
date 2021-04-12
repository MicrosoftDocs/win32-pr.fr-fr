---
title: Méthode ChangeMode de la classe Win32_TerminalServiceSetting
description: La méthode ChangeMode définit le type de licence du serveur actuel de l’hôte de session Bureau à distance (hôte de session Bureau à distance).
ms.assetid: 293483ee-51ce-4cd4-ba13-6c7c02bbdbbf
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ChangeMode
- Services Bureau à distance de la méthode ChangeMode, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode ChangeMode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.ChangeMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880fcab8aa68e49c6b3c00278b90635686de6168
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384547"
---
# <a name="changemode-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="afe13-106">Méthode ChangeMode de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="afe13-106">ChangeMode method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="afe13-107">La méthode **ChangeMode** définit le type de licence du serveur actuel de l’hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="afe13-107">The **ChangeMode** method sets the licensing type of the current Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="afe13-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="afe13-108">Syntax</span></span>


```mof
uint32 ChangeMode(
  [in] uint32 LicensingType
);
```



## <a name="parameters"></a><span data-ttu-id="afe13-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="afe13-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afe13-110">*LicensingType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="afe13-110">*LicensingType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afe13-111">Type de licence à définir en fonction du mode de serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="afe13-111">The licensing type to set based on the RD Session Host server mode.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="afe13-112"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="afe13-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="afe13-113">Serveur hôte de session Bureau à distance personnel.</span><span class="sxs-lookup"><span data-stu-id="afe13-113">Personal RD Session Host server.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="afe13-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="afe13-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="afe13-115">Bureau à distance pour l’administration.</span><span class="sxs-lookup"><span data-stu-id="afe13-115">Remote desktop for administration.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="afe13-116"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="afe13-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="afe13-117">Par appareil/par siège.</span><span class="sxs-lookup"><span data-stu-id="afe13-117">Per device/per seat.</span></span> <span data-ttu-id="afe13-118">Valide pour les serveurs d’applications.</span><span class="sxs-lookup"><span data-stu-id="afe13-118">Valid for application servers.</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="afe13-119"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="afe13-119"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="afe13-120">Par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="afe13-120">Per User.</span></span> <span data-ttu-id="afe13-121">Valide pour les serveurs d’applications.</span><span class="sxs-lookup"><span data-stu-id="afe13-121">Valid for application servers.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afe13-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="afe13-122">Return value</span></span>

<span data-ttu-id="afe13-123">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="afe13-123">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="afe13-124">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="afe13-124">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="afe13-125">Notes</span><span class="sxs-lookup"><span data-stu-id="afe13-125">Remarks</span></span>

<span data-ttu-id="afe13-126">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="afe13-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="afe13-127">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="afe13-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="afe13-128">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="afe13-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="afe13-129">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="afe13-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="afe13-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="afe13-130">Requirements</span></span>



| <span data-ttu-id="afe13-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="afe13-131">Requirement</span></span> | <span data-ttu-id="afe13-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="afe13-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="afe13-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="afe13-133">Minimum supported client</span></span><br/> | <span data-ttu-id="afe13-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="afe13-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="afe13-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="afe13-135">Minimum supported server</span></span><br/> | <span data-ttu-id="afe13-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afe13-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="afe13-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="afe13-137">Namespace</span></span><br/>                | <span data-ttu-id="afe13-138">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="afe13-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="afe13-139">MOF</span><span class="sxs-lookup"><span data-stu-id="afe13-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="afe13-140"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="afe13-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="afe13-141">DLL</span><span class="sxs-lookup"><span data-stu-id="afe13-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afe13-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afe13-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afe13-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="afe13-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afe13-144">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="afe13-144">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

