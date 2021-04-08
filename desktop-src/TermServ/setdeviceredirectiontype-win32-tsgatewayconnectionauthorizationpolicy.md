---
title: Méthode SetDeviceRedirectionType de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Définit la propriété DeviceRedirectionType, qui contrôle les appareils qui seront redirigés.
ms.assetid: d97a0a7d-a08e-4703-b0f0-ba5d20688dc8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetDeviceRedirectionType
- Services Bureau à distance de la méthode SetDeviceRedirectionType, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode SetDeviceRedirectionType
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetDeviceRedirectionType
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98b369e0b6031aa503e2f7f55860d004f63b7f93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942045"
---
# <a name="setdeviceredirectiontype-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="04dea-106">Méthode SetDeviceRedirectionType de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="04dea-106">SetDeviceRedirectionType method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="04dea-107">Définit la propriété **DeviceRedirectionType** , qui contrôle les appareils qui seront redirigés.</span><span class="sxs-lookup"><span data-stu-id="04dea-107">Sets the **DeviceRedirectionType** property, which controls which devices will be redirected.</span></span>

## <a name="syntax"></a><span data-ttu-id="04dea-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04dea-108">Syntax</span></span>


```mof
uint32 SetDeviceRedirectionType(
  [in] uint32 DeviceRedirectionType
);
```



## <a name="parameters"></a><span data-ttu-id="04dea-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04dea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04dea-110">*DeviceRedirectionType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="04dea-110">*DeviceRedirectionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04dea-111">Type de redirection de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="04dea-111">The device redirection type.</span></span>

<dt>

<span data-ttu-id="04dea-112">0</span><span class="sxs-lookup"><span data-stu-id="04dea-112">0</span></span>
</dt> <dd>

<span data-ttu-id="04dea-113">Tous les appareils seront redirigés.</span><span class="sxs-lookup"><span data-stu-id="04dea-113">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="04dea-114">1</span><span class="sxs-lookup"><span data-stu-id="04dea-114">1</span></span>
</dt> <dd>

<span data-ttu-id="04dea-115">Aucun appareil n’est redirigé.</span><span class="sxs-lookup"><span data-stu-id="04dea-115">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="04dea-116">2</span><span class="sxs-lookup"><span data-stu-id="04dea-116">2</span></span>
</dt> <dd>

<span data-ttu-id="04dea-117">Les appareils spécifiés ne seront pas redirigés.</span><span class="sxs-lookup"><span data-stu-id="04dea-117">Specified devices will not be redirected.</span></span> <span data-ttu-id="04dea-118">Les propriétés **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled** et **PlugAndPlayDevicesDisabled** contrôlent les appareils qui ne seront pas redirigés.</span><span class="sxs-lookup"><span data-stu-id="04dea-118">The **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled**, and **PlugAndPlayDevicesDisabled** properties control which devices will not be redirected.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04dea-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="04dea-119">Return value</span></span>

<span data-ttu-id="04dea-120">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="04dea-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="04dea-121">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="04dea-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="04dea-122">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="04dea-122">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="04dea-123">Notes</span><span class="sxs-lookup"><span data-stu-id="04dea-123">Remarks</span></span>

<span data-ttu-id="04dea-124">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="04dea-124">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="04dea-125">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="04dea-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="04dea-126">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="04dea-126">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="04dea-127">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="04dea-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="04dea-128">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="04dea-128">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="04dea-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04dea-129">Requirements</span></span>



| <span data-ttu-id="04dea-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04dea-130">Requirement</span></span> | <span data-ttu-id="04dea-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="04dea-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="04dea-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04dea-132">Minimum supported client</span></span><br/> | <span data-ttu-id="04dea-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="04dea-133">None supported</span></span><br/>                                                                |
| <span data-ttu-id="04dea-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04dea-134">Minimum supported server</span></span><br/> | <span data-ttu-id="04dea-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04dea-135">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="04dea-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="04dea-136">Namespace</span></span><br/>                | <span data-ttu-id="04dea-137">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="04dea-137">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="04dea-138">MOF</span><span class="sxs-lookup"><span data-stu-id="04dea-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04dea-139"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04dea-139"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="04dea-140">DLL</span><span class="sxs-lookup"><span data-stu-id="04dea-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04dea-141"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04dea-141"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="04dea-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04dea-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04dea-143">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="04dea-143">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

