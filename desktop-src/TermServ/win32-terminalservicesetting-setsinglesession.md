---
title: Méthode SetSingleSession de la classe Win32_TerminalServiceSetting
description: La méthode SetSingleSession définit la propriété SingleSession de la classe.
ms.assetid: 67ccfa9d-86a5-4501-9d61-c7f1677ec3d5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetSingleSession
- Services Bureau à distance de la méthode SetSingleSession, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode SetSingleSession
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetSingleSession
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a6ff702020b7682938b7174c65623eba30076a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509557"
---
# <a name="setsinglesession-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="99ac8-106">Méthode SetSingleSession de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="99ac8-106">SetSingleSession method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="99ac8-107">La méthode **SetSingleSession** définit la propriété **SingleSession** de la classe.</span><span class="sxs-lookup"><span data-stu-id="99ac8-107">The **SetSingleSession** method sets the **SingleSession** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="99ac8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99ac8-108">Syntax</span></span>


```mof
uint32 SetSingleSession(
  [in] uint32 SingleSession
);
```



## <a name="parameters"></a><span data-ttu-id="99ac8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99ac8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99ac8-110">*SingleSession* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="99ac8-110">*SingleSession* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99ac8-111">Indicateur de désactivation ou d’activation de la propriété **SingleSession** , qui détermine si les utilisateurs sont limités à une ou plusieurs sessions services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="99ac8-111">Flag disabling or enabling the **SingleSession** property, which determines whether users are limited to one or more Remote Desktop Services sessions.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="99ac8-112"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="99ac8-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="99ac8-113">Désactivez la propriété.</span><span class="sxs-lookup"><span data-stu-id="99ac8-113">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="99ac8-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="99ac8-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="99ac8-115">Activez la propriété.</span><span class="sxs-lookup"><span data-stu-id="99ac8-115">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99ac8-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="99ac8-116">Return value</span></span>

<span data-ttu-id="99ac8-117">Retourne une réussite en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="99ac8-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="99ac8-118">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="99ac8-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="99ac8-119">Notes</span><span class="sxs-lookup"><span data-stu-id="99ac8-119">Remarks</span></span>

<span data-ttu-id="99ac8-120">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="99ac8-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="99ac8-121">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="99ac8-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="99ac8-122">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="99ac8-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="99ac8-123">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="99ac8-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="99ac8-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99ac8-124">Requirements</span></span>



| <span data-ttu-id="99ac8-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99ac8-125">Requirement</span></span> | <span data-ttu-id="99ac8-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="99ac8-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99ac8-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99ac8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="99ac8-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99ac8-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="99ac8-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99ac8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="99ac8-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99ac8-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="99ac8-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="99ac8-131">Namespace</span></span><br/>                | <span data-ttu-id="99ac8-132">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="99ac8-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="99ac8-133">MOF</span><span class="sxs-lookup"><span data-stu-id="99ac8-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99ac8-134"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="99ac8-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="99ac8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="99ac8-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99ac8-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99ac8-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99ac8-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99ac8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99ac8-138">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="99ac8-138">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

