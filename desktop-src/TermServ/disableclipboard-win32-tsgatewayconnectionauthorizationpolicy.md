---
title: Méthode DisableClipboard de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Définit la propriété ClipboardDisabled. Si la propriété DeviceRedirectionType a la valeur \ 0034 ; 2 \ 0034 ;, la propriété ClipboardDisabled contrôle la redirection du presse-papiers pour les sessions établies par le biais du serveur de passerelle Bureau à distance (passerelle Bureau à distance).
ms.assetid: c53fc802-958b-452d-9af9-0ce89ed46079
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode DisableClipboard
- Services Bureau à distance de la méthode DisableClipboard, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode DisableClipboard
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableClipboard
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23ae2070a35fa31f1c9d9ad31e9e632e31c0193f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512365"
---
# <a name="disableclipboard-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="30586-107">Méthode DisableClipboard de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="30586-107">DisableClipboard method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="30586-108">Définit la propriété **ClipboardDisabled** .</span><span class="sxs-lookup"><span data-stu-id="30586-108">Sets the **ClipboardDisabled** property.</span></span> <span data-ttu-id="30586-109">Si la propriété **DeviceRedirectionType** a la valeur « 2 », la propriété **ClipboardDisabled** contrôle la redirection du presse-papiers pour les sessions établies par le biais du serveur de passerelle Bureau à distance (passerelle Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="30586-109">If the **DeviceRedirectionType** property has a value of "2", the **ClipboardDisabled** property controls redirection of the clipboard for sessions that are established through the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="30586-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30586-110">Syntax</span></span>


```mof
uint32 DisableClipboard(
  [in] boolean Disabled
);
```



## <a name="parameters"></a><span data-ttu-id="30586-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30586-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30586-112">*Désactivé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30586-112">*Disabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30586-113">Nouvelle valeur de la propriété **ClipboardDisabled** .</span><span class="sxs-lookup"><span data-stu-id="30586-113">New value for the **ClipboardDisabled** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30586-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30586-114">Return value</span></span>

<span data-ttu-id="30586-115">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="30586-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="30586-116">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="30586-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="30586-117">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="30586-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="30586-118">Notes</span><span class="sxs-lookup"><span data-stu-id="30586-118">Remarks</span></span>

<span data-ttu-id="30586-119">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="30586-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="30586-120">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="30586-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="30586-121">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="30586-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="30586-122">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="30586-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="30586-123">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="30586-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="30586-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30586-124">Requirements</span></span>



| <span data-ttu-id="30586-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30586-125">Requirement</span></span> | <span data-ttu-id="30586-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="30586-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="30586-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30586-127">Minimum supported client</span></span><br/> | <span data-ttu-id="30586-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="30586-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="30586-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30586-129">Minimum supported server</span></span><br/> | <span data-ttu-id="30586-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30586-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="30586-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="30586-131">Namespace</span></span><br/>                | <span data-ttu-id="30586-132">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="30586-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="30586-133">MOF</span><span class="sxs-lookup"><span data-stu-id="30586-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30586-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="30586-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="30586-135">DLL</span><span class="sxs-lookup"><span data-stu-id="30586-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30586-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30586-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="30586-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30586-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30586-138">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="30586-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

