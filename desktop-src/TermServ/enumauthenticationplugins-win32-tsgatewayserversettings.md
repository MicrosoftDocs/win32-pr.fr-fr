---
title: Méthode EnumAuthenticationPlugins de la classe Win32_TSGatewayServerSettings
description: Énumère tous les plug-ins d’authentification inscrits.
ms.assetid: a5c1859d-e20c-4c72-aef5-ef9941edf73e
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode EnumAuthenticationPlugins
- Services Bureau à distance de la méthode EnumAuthenticationPlugins, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode EnumAuthenticationPlugins
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnumAuthenticationPlugins
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0cd9d059a79749f657c6191e68e7bcd08555cb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512555"
---
# <a name="enumauthenticationplugins-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="c67b8-106">Méthode EnumAuthenticationPlugins de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="c67b8-106">EnumAuthenticationPlugins method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="c67b8-107">Énumère tous les plug-ins d’authentification inscrits.</span><span class="sxs-lookup"><span data-stu-id="c67b8-107">Enumerates all registered authentication plug-ins.</span></span>

## <a name="syntax"></a><span data-ttu-id="c67b8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c67b8-108">Syntax</span></span>


```mof
uint32 EnumAuthenticationPlugins(
  [out] string PluginNames[],
  [out] string CLSIDs[],
  [out] string Descriptions[]
);
```



## <a name="parameters"></a><span data-ttu-id="c67b8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c67b8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c67b8-110">*PluginNames* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c67b8-110">*PluginNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c67b8-111">Type : **chaîne \[ \]**</span><span class="sxs-lookup"><span data-stu-id="c67b8-111">Type: **string\[\]**</span></span>

<span data-ttu-id="c67b8-112">Tableau de **chaînes** qui reçoit les noms des plug-ins d’authentification inscrits.</span><span class="sxs-lookup"><span data-stu-id="c67b8-112">A **string** array that receives the names of the registered authentication plug-ins.</span></span>

</dd> <dt>

<span data-ttu-id="c67b8-113">*CLSID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c67b8-113">*CLSIDs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c67b8-114">Type : **chaîne \[ \]**</span><span class="sxs-lookup"><span data-stu-id="c67b8-114">Type: **string\[\]**</span></span>

<span data-ttu-id="c67b8-115">Tableau de **chaînes** qui reçoit les CLSID des plug-ins d’authentification inscrits.</span><span class="sxs-lookup"><span data-stu-id="c67b8-115">A **string** array that receives the CLSIDs of the registered authentication plug-ins.</span></span>

</dd> <dt>

<span data-ttu-id="c67b8-116">*Descriptions* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c67b8-116">*Descriptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c67b8-117">Type : **chaîne \[ \]**</span><span class="sxs-lookup"><span data-stu-id="c67b8-117">Type: **string\[\]**</span></span>

<span data-ttu-id="c67b8-118">Tableau de **chaînes** qui reçoit les descriptions des plug-ins d’authentification inscrits.</span><span class="sxs-lookup"><span data-stu-id="c67b8-118">A **string** array that receives the descriptions of the registered authentication plug-ins.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c67b8-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c67b8-119">Return value</span></span>

<span data-ttu-id="c67b8-120">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c67b8-120">Type: **uint32**</span></span>

<span data-ttu-id="c67b8-121">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="c67b8-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c67b8-122">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="c67b8-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c67b8-123">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c67b8-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c67b8-124">Notes</span><span class="sxs-lookup"><span data-stu-id="c67b8-124">Remarks</span></span>

<span data-ttu-id="c67b8-125">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c67b8-125">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c67b8-126">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="c67b8-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c67b8-127">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c67b8-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c67b8-128">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="c67b8-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c67b8-129">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c67b8-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c67b8-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c67b8-130">Requirements</span></span>



| <span data-ttu-id="c67b8-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c67b8-131">Requirement</span></span> | <span data-ttu-id="c67b8-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="c67b8-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c67b8-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c67b8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c67b8-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c67b8-134">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c67b8-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c67b8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c67b8-136">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c67b8-136">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="c67b8-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c67b8-137">Namespace</span></span><br/>                | <span data-ttu-id="c67b8-138">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="c67b8-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c67b8-139">MOF</span><span class="sxs-lookup"><span data-stu-id="c67b8-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c67b8-140"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c67b8-140"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c67b8-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c67b8-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c67b8-142"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c67b8-142"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c67b8-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c67b8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c67b8-144">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="c67b8-144">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

