---
title: Méthode DisablePrinters de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Définit la propriété PrintersDisabled. Si la propriété DeviceRedirectionType a la valeur \ 0034 ; 2 \ 0034 ;, la propriété PrintersDisabled contrôle la redirection des imprimantes pour les sessions établies par le biais du serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: bf58d226-e3de-4c2b-aaa9-9e7ddbf49d31
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode DisablePrinters
- Services Bureau à distance de la méthode DisablePrinters, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode DisablePrinters
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisablePrinters
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1625425170bd5e29b953db8299048261e9351bff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509084"
---
# <a name="disableprinters-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="bbe56-107">Méthode DisablePrinters de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="bbe56-107">DisablePrinters method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="bbe56-108">Définit la propriété **PrintersDisabled** .</span><span class="sxs-lookup"><span data-stu-id="bbe56-108">Sets the **PrintersDisabled** property.</span></span> <span data-ttu-id="bbe56-109">Si la propriété **DeviceRedirectionType** a la valeur « 2 », la propriété **PrintersDisabled** contrôle la redirection des imprimantes pour les sessions établies par le biais du serveur de passerelle Bureau à distance (passerelle Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="bbe56-109">If the **DeviceRedirectionType** property has a value of "2", the **PrintersDisabled** property controls redirection of the printers for sessions that are established through the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbe56-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bbe56-110">Syntax</span></span>


```mof
uint32 DisablePrinters(
  [in] boolean Disabled
);
```



## <a name="parameters"></a><span data-ttu-id="bbe56-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bbe56-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbe56-112">*Désactivé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bbe56-112">*Disabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbe56-113">Nouvelle valeur de la propriété **PrintersDisabled** .</span><span class="sxs-lookup"><span data-stu-id="bbe56-113">New value for the **PrintersDisabled** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbe56-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bbe56-114">Return value</span></span>

<span data-ttu-id="bbe56-115">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="bbe56-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="bbe56-116">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="bbe56-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="bbe56-117">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bbe56-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bbe56-118">Notes</span><span class="sxs-lookup"><span data-stu-id="bbe56-118">Remarks</span></span>

<span data-ttu-id="bbe56-119">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="bbe56-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="bbe56-120">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="bbe56-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bbe56-121">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bbe56-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bbe56-122">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="bbe56-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bbe56-123">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bbe56-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bbe56-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bbe56-124">Requirements</span></span>



| <span data-ttu-id="bbe56-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bbe56-125">Requirement</span></span> | <span data-ttu-id="bbe56-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbe56-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbe56-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbe56-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bbe56-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbe56-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="bbe56-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbe56-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bbe56-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bbe56-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bbe56-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bbe56-131">Namespace</span></span><br/>                | <span data-ttu-id="bbe56-132">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="bbe56-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="bbe56-133">MOF</span><span class="sxs-lookup"><span data-stu-id="bbe56-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bbe56-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bbe56-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="bbe56-135">DLL</span><span class="sxs-lookup"><span data-stu-id="bbe56-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbe56-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbe56-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bbe56-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbe56-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbe56-138">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="bbe56-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

