---
title: Méthode SetPolicyPropertyName de la classe Win32_TerminalServiceSetting
description: La méthode SetPolicyPropertyName définit la propriété DeleteTempFolders, UseTempFolders ou Help pour la classe.
ms.assetid: 18d9927a-b7db-46c7-90ee-00da6de06202
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetPolicyPropertyName
- Services Bureau à distance de la méthode SetPolicyPropertyName, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode SetPolicyPropertyName
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPolicyPropertyName
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f49732fa916dd3c37539dc35d6cef7a4d920d81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466718"
---
# <a name="setpolicypropertyname-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="1e2b5-106">Méthode SetPolicyPropertyName de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="1e2b5-106">SetPolicyPropertyName method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="1e2b5-107">La méthode **SetPolicyPropertyName** définit la propriété **DeleteTempFolders**, **UseTempFolders** ou **Help** pour la classe.</span><span class="sxs-lookup"><span data-stu-id="1e2b5-107">The **SetPolicyPropertyName** method sets the **DeleteTempFolders**, **UseTempFolders** or **Help** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e2b5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e2b5-108">Syntax</span></span>


```mof
uint32 SetPolicyPropertyName(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a><span data-ttu-id="1e2b5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e2b5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e2b5-110">*PropertyName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e2b5-110">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e2b5-111">Spécifie la propriété de stratégie définie par la méthode.</span><span class="sxs-lookup"><span data-stu-id="1e2b5-111">Specifies the policy property that the method is setting.</span></span>

<dt>

<span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>

<span data-ttu-id="1e2b5-112"><span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>**DeleteTempFolders**</span><span class="sxs-lookup"><span data-stu-id="1e2b5-112"><span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>**DeleteTempFolders**</span></span>


</dt> <dd>

<span data-ttu-id="1e2b5-113">La méthode définit la propriété **DeleteTempFolders** .</span><span class="sxs-lookup"><span data-stu-id="1e2b5-113">The method is setting the **DeleteTempFolders** property.</span></span>

</dd> <dt>

<span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>

<span data-ttu-id="1e2b5-114"><span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>**UseTempFolders**</span><span class="sxs-lookup"><span data-stu-id="1e2b5-114"><span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>**UseTempFolders**</span></span>


</dt> <dd>

<span data-ttu-id="1e2b5-115">La méthode définit la propriété **UseTempFolders** .</span><span class="sxs-lookup"><span data-stu-id="1e2b5-115">The method is setting the **UseTempFolders** property.</span></span>

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>

<span data-ttu-id="1e2b5-116"><span id="Help"></span><span id="help"></span><span id="HELP"></span>**Aide**</span><span class="sxs-lookup"><span data-stu-id="1e2b5-116"><span id="Help"></span><span id="help"></span><span id="HELP"></span>**Help**</span></span>


</dt> <dd>

<span data-ttu-id="1e2b5-117">La méthode définit la propriété **d’aide** .</span><span class="sxs-lookup"><span data-stu-id="1e2b5-117">The method is setting the **Help** property.</span></span>

<span data-ttu-id="1e2b5-118">**Remarque :**  **l’aide** n’est pas prise en charge</span><span class="sxs-lookup"><span data-stu-id="1e2b5-118">**Note**  **Help** is not supported</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1e2b5-119">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e2b5-119">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e2b5-120">Valeur qui indique s’il faut activer ou désactiver la propriété spécifiée par le paramètre *PropertyName* .</span><span class="sxs-lookup"><span data-stu-id="1e2b5-120">Value that indicates whether to enable or disable the property specified by the *PropertyName* parameter.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="1e2b5-121"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="1e2b5-121"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="1e2b5-122">Désactivez la propriété.</span><span class="sxs-lookup"><span data-stu-id="1e2b5-122">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="1e2b5-123"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="1e2b5-123"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="1e2b5-124">Activez la propriété.</span><span class="sxs-lookup"><span data-stu-id="1e2b5-124">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e2b5-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e2b5-125">Return value</span></span>

<span data-ttu-id="1e2b5-126">Retourne une réussite en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="1e2b5-126">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="1e2b5-127">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="1e2b5-127">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="1e2b5-128">La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="1e2b5-128">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e2b5-129">Notes</span><span class="sxs-lookup"><span data-stu-id="1e2b5-129">Remarks</span></span>

<span data-ttu-id="1e2b5-130">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="1e2b5-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1e2b5-131">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1e2b5-131">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1e2b5-132">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="1e2b5-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1e2b5-133">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1e2b5-133">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e2b5-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e2b5-134">Requirements</span></span>



| <span data-ttu-id="1e2b5-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e2b5-135">Requirement</span></span> | <span data-ttu-id="1e2b5-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e2b5-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e2b5-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e2b5-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1e2b5-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e2b5-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1e2b5-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e2b5-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1e2b5-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e2b5-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1e2b5-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1e2b5-141">Namespace</span></span><br/>                | <span data-ttu-id="1e2b5-142">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="1e2b5-142">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1e2b5-143">MOF</span><span class="sxs-lookup"><span data-stu-id="1e2b5-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e2b5-144"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e2b5-144"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e2b5-145">DLL</span><span class="sxs-lookup"><span data-stu-id="1e2b5-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e2b5-146"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e2b5-146"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e2b5-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e2b5-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e2b5-148">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="1e2b5-148">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

