---
title: Méthode SetFallbackPrintDriverType de la classe Win32_TerminalServiceSetting
description: La méthode SetFallbackPrintDriverType définit la propriété FallbackPrintDriverType de la classe.
ms.assetid: be738134-199a-41a6-b2f8-cccfa14fa02b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetFallbackPrintDriverType
- Services Bureau à distance de la méthode SetFallbackPrintDriverType, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode SetFallbackPrintDriverType
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetFallbackPrintDriverType
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e445fef86970e89d5b0f09abebecd40f49ab7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033182"
---
# <a name="setfallbackprintdrivertype-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="8f796-106">Méthode SetFallbackPrintDriverType de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="8f796-106">SetFallbackPrintDriverType method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="8f796-107">La méthode **SetFallbackPrintDriverType** définit la propriété **FallbackPrintDriverType** de la classe.</span><span class="sxs-lookup"><span data-stu-id="8f796-107">The **SetFallbackPrintDriverType** method sets the **FallbackPrintDriverType** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f796-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f796-108">Syntax</span></span>


```mof
uint32 SetFallbackPrintDriverType(
  [in] uint32 FallbackPrintDriverType
);
```



## <a name="parameters"></a><span data-ttu-id="8f796-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f796-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f796-110">*FallbackPrintDriverType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8f796-110">*FallbackPrintDriverType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f796-111">Définit la propriété **FallbackPrintDriverType** qui autorise ou refuse les nouvelles connexions de services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="8f796-111">Sets the **FallbackPrintDriverType** property which allows or denies new Remote Desktop Services connections.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="8f796-112"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="8f796-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="8f796-113">Aucun pilote de secours.</span><span class="sxs-lookup"><span data-stu-id="8f796-113">No fallback drivers.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="8f796-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="8f796-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="8f796-115">Meilleure hypothèse.</span><span class="sxs-lookup"><span data-stu-id="8f796-115">Best guess.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="8f796-116"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="8f796-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="8f796-117">Meilleure hypothèse.</span><span class="sxs-lookup"><span data-stu-id="8f796-117">Best guess.</span></span> <span data-ttu-id="8f796-118">Si aucune correspondance n’est trouvée, vous pouvez revenir à Hewlett-Packard PCL (Printer Control Language).</span><span class="sxs-lookup"><span data-stu-id="8f796-118">If no match is found, fallback to Hewlett-Packard Printer Control Language (PCL).</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="8f796-119"><span id="3"></span>**1,3**</span><span class="sxs-lookup"><span data-stu-id="8f796-119"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="8f796-120">Meilleure hypothèse.</span><span class="sxs-lookup"><span data-stu-id="8f796-120">Best guess.</span></span> <span data-ttu-id="8f796-121">Si aucune correspondance n’est trouvée, basculez vers PostScript (PS).</span><span class="sxs-lookup"><span data-stu-id="8f796-121">If no match is found, fallback to Postscript (PS).</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="8f796-122"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="8f796-122"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="8f796-123">Meilleure hypothèse.</span><span class="sxs-lookup"><span data-stu-id="8f796-123">Best guess.</span></span> <span data-ttu-id="8f796-124">Si aucune correspondance n’est trouvée, affichez les pilotes PS et PCL.</span><span class="sxs-lookup"><span data-stu-id="8f796-124">If no match is found, show both PS and PCL drivers.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f796-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8f796-125">Return value</span></span>

<span data-ttu-id="8f796-126">Retourne une réussite en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="8f796-126">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="8f796-127">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="8f796-127">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="8f796-128">La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8f796-128">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f796-129">Notes</span><span class="sxs-lookup"><span data-stu-id="8f796-129">Remarks</span></span>

<span data-ttu-id="8f796-130">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="8f796-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8f796-131">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8f796-131">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8f796-132">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="8f796-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8f796-133">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8f796-133">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f796-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f796-134">Requirements</span></span>



| <span data-ttu-id="8f796-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f796-135">Requirement</span></span> | <span data-ttu-id="8f796-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f796-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f796-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f796-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8f796-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f796-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f796-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f796-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8f796-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f796-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f796-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8f796-141">Namespace</span></span><br/>                | <span data-ttu-id="8f796-142">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="8f796-142">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8f796-143">MOF</span><span class="sxs-lookup"><span data-stu-id="8f796-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f796-144"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f796-144"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f796-145">DLL</span><span class="sxs-lookup"><span data-stu-id="8f796-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f796-146"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f796-146"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f796-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f796-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f796-148">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="8f796-148">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

