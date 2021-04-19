---
title: Méthode SetClientProperty de la classe Win32_TSClientSetting
description: La méthode SetClientProperty définit la propriété LPTPortMapping, COMPortMapping, AudioMapping, ClipboardMapping, DriveMapping ou WindowsPrinterMapping pour la classe.
ms.assetid: a8ad922f-d768-4708-9a67-c6b00580baed
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetClientProperty
- Services Bureau à distance de la méthode SetClientProperty, classe Win32_TSClientSetting
- Win32_TSClientSetting de la classe Services Bureau à distance, méthode SetClientProperty
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetClientProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89bfdfd7c7f2c4b23f76b50ab671d74541f9dbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510317"
---
# <a name="setclientproperty-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="25504-106">Méthode SetClientProperty de la \_ classe Win32 TSClientSetting</span><span class="sxs-lookup"><span data-stu-id="25504-106">SetClientProperty method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="25504-107">La méthode **SetClientProperty** définit la **propriété LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping** ou **WindowsPrinterMapping** pour la classe.</span><span class="sxs-lookup"><span data-stu-id="25504-107">The **SetClientProperty** method sets the **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping**, or **WindowsPrinterMapping** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="25504-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25504-108">Syntax</span></span>


```mof
uint32 SetClientProperty(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a><span data-ttu-id="25504-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25504-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25504-110">*PropertyName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="25504-110">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25504-111">Spécifie la propriété cliente définie par la méthode.</span><span class="sxs-lookup"><span data-stu-id="25504-111">Specifies the client property that the method is setting.</span></span>

<dt>

<span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>

<span data-ttu-id="25504-112"><span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>**AudioMapping**</span><span class="sxs-lookup"><span data-stu-id="25504-112"><span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>**AudioMapping**</span></span>


</dt> <dd>

<span data-ttu-id="25504-113">La méthode définit la propriété **AudioMapping** .</span><span class="sxs-lookup"><span data-stu-id="25504-113">The method is setting the **AudioMapping** property.</span></span>

</dd> <dt>

<span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>

<span data-ttu-id="25504-114"><span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>**ClipboardMapping**</span><span class="sxs-lookup"><span data-stu-id="25504-114"><span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>**ClipboardMapping**</span></span>


</dt> <dd>

<span data-ttu-id="25504-115">La méthode définit la propriété **ClipboardMapping** .</span><span class="sxs-lookup"><span data-stu-id="25504-115">The method is setting the **ClipboardMapping** property.</span></span>

</dd> <dt>

<span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>

<span data-ttu-id="25504-116"><span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>**COMPortMapping**</span><span class="sxs-lookup"><span data-stu-id="25504-116"><span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>**COMPortMapping**</span></span>


</dt> <dd>

<span data-ttu-id="25504-117">La méthode définit la propriété **COMPortMapping** .</span><span class="sxs-lookup"><span data-stu-id="25504-117">The method is setting the **COMPortMapping** property.</span></span>

</dd> <dt>

<span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>

<span data-ttu-id="25504-118"><span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>**DriveMapping**</span><span class="sxs-lookup"><span data-stu-id="25504-118"><span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>**DriveMapping**</span></span>


</dt> <dd>

<span data-ttu-id="25504-119">La méthode définit la propriété **DriveMapping** .</span><span class="sxs-lookup"><span data-stu-id="25504-119">The method is setting the **DriveMapping** property.</span></span>

</dd> <dt>

<span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>

<span data-ttu-id="25504-120"><span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>**LPTPortMapping**</span><span class="sxs-lookup"><span data-stu-id="25504-120"><span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>**LPTPortMapping**</span></span>


</dt> <dd>

<span data-ttu-id="25504-121">La méthode définit la propriété **LPTPortMapping** .</span><span class="sxs-lookup"><span data-stu-id="25504-121">The method is setting the **LPTPortMapping** property.</span></span>

</dd> <dt>

<span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>

<span data-ttu-id="25504-122"><span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>**PNPRedirection**</span><span class="sxs-lookup"><span data-stu-id="25504-122"><span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>**PNPRedirection**</span></span>


</dt> <dd>

<span data-ttu-id="25504-123">La méthode définit la propriété **PNPRedirection** .</span><span class="sxs-lookup"><span data-stu-id="25504-123">The method is setting the **PNPRedirection** property.</span></span>

</dd> <dt>

<span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>

<span data-ttu-id="25504-124"><span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>**WindowsPrinterMapping**</span><span class="sxs-lookup"><span data-stu-id="25504-124"><span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>**WindowsPrinterMapping**</span></span>


</dt> <dd>

<span data-ttu-id="25504-125">La méthode définit la propriété **WindowsPrinterMapping** .</span><span class="sxs-lookup"><span data-stu-id="25504-125">The method is setting the **WindowsPrinterMapping** property.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="25504-126">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="25504-126">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25504-127">Valeur qui indique s’il faut activer ou désactiver la propriété spécifiée par le paramètre *PropertyName* .</span><span class="sxs-lookup"><span data-stu-id="25504-127">Value that indicates whether to enable or disable the property specified by the *PropertyName* parameter.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="25504-128"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="25504-128"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="25504-129">Désactivez la propriété.</span><span class="sxs-lookup"><span data-stu-id="25504-129">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="25504-130"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="25504-130"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="25504-131">Activez la propriété.</span><span class="sxs-lookup"><span data-stu-id="25504-131">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25504-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="25504-132">Return value</span></span>

<span data-ttu-id="25504-133">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="25504-133">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="25504-134">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="25504-134">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="25504-135">La méthode retourne une erreur si la propriété cliente spécifiée n’est pas sous contrôle de stratégie de groupe ou si le paramètre de propriété n’est pas éligible pour la substitution par le serveur.</span><span class="sxs-lookup"><span data-stu-id="25504-135">The method returns an error if the specified client property is not under group policy control or if the property setting is not eligible for override by the server.</span></span>

## <a name="remarks"></a><span data-ttu-id="25504-136">Notes</span><span class="sxs-lookup"><span data-stu-id="25504-136">Remarks</span></span>

<span data-ttu-id="25504-137">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="25504-137">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="25504-138">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="25504-138">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="25504-139">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="25504-139">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="25504-140">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="25504-140">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="25504-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25504-141">Requirements</span></span>



| <span data-ttu-id="25504-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25504-142">Requirement</span></span> | <span data-ttu-id="25504-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="25504-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25504-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25504-144">Minimum supported client</span></span><br/> | <span data-ttu-id="25504-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25504-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="25504-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25504-146">Minimum supported server</span></span><br/> | <span data-ttu-id="25504-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25504-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="25504-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="25504-148">Namespace</span></span><br/>                | <span data-ttu-id="25504-149">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="25504-149">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="25504-150">MOF</span><span class="sxs-lookup"><span data-stu-id="25504-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25504-151"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25504-151"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="25504-152">DLL</span><span class="sxs-lookup"><span data-stu-id="25504-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25504-153"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25504-153"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25504-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25504-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25504-155">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="25504-155">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

