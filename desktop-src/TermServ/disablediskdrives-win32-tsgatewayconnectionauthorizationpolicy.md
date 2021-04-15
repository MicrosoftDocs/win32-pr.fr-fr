---
title: Méthode DisableDiskDrives de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Définit la propriété DiskDrivesDisabled.
ms.assetid: bdc4a923-bda7-464a-95eb-95231374ac93
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode DisableDiskDrives
- Services Bureau à distance de la méthode DisableDiskDrives, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode DisableDiskDrives
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableDiskDrives
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63938ccae6e93e23bd754c1d18ede0008fe92257
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384063"
---
# <a name="disablediskdrives-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="d96fb-106">Méthode DisableDiskDrives de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="d96fb-106">DisableDiskDrives method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="d96fb-107">Définit la propriété **DiskDrivesDisabled** .</span><span class="sxs-lookup"><span data-stu-id="d96fb-107">Sets the **DiskDrivesDisabled** property.</span></span> <span data-ttu-id="d96fb-108">Si la propriété **DeviceRedirectionType** a la valeur « 2 », la propriété **DiskDrivesDisabled** contrôle la redirection des lecteurs de disque client pour les sessions établies par le biais du serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="d96fb-108">If the **DeviceRedirectionType** property has a value of "2", the **DiskDrivesDisabled** property controls redirection of the client disk drives for sessions that are established through the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="d96fb-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d96fb-109">Syntax</span></span>


```mof
uint32 DisableDiskDrives(
  [in] boolean Disabled
);
```



## <a name="parameters"></a><span data-ttu-id="d96fb-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d96fb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d96fb-111">*Désactivé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d96fb-111">*Disabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d96fb-112">Nouvelle valeur de la propriété **DiskDrivesDisabled** .</span><span class="sxs-lookup"><span data-stu-id="d96fb-112">New value for the **DiskDrivesDisabled** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d96fb-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d96fb-113">Return value</span></span>

<span data-ttu-id="d96fb-114">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="d96fb-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d96fb-115">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="d96fb-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d96fb-116">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d96fb-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d96fb-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d96fb-117">Remarks</span></span>

<span data-ttu-id="d96fb-118">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="d96fb-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d96fb-119">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="d96fb-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d96fb-120">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d96fb-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d96fb-121">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="d96fb-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d96fb-122">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d96fb-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d96fb-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d96fb-123">Requirements</span></span>



| <span data-ttu-id="d96fb-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d96fb-124">Requirement</span></span> | <span data-ttu-id="d96fb-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="d96fb-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d96fb-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d96fb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d96fb-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d96fb-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d96fb-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d96fb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d96fb-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d96fb-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d96fb-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d96fb-130">Namespace</span></span><br/>                | <span data-ttu-id="d96fb-131">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="d96fb-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="d96fb-132">MOF</span><span class="sxs-lookup"><span data-stu-id="d96fb-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d96fb-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d96fb-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="d96fb-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d96fb-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d96fb-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d96fb-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="d96fb-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d96fb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d96fb-137">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="d96fb-137">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

