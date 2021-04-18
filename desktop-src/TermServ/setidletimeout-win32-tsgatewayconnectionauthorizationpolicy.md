---
title: Méthode SetIdleTimeout de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Définit la propriété IdleTimeout.
ms.assetid: 162224dd-e4d4-483f-9ec4-b87731bc5014
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetIdleTimeout
- Services Bureau à distance de la méthode SetIdleTimeout, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode SetIdleTimeout
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetIdleTimeout
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c166311477dc9de94ca6c9614e14ac98907b406
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106516295"
---
# <a name="setidletimeout-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="10a77-106">Méthode SetIdleTimeout de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="10a77-106">SetIdleTimeout method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="10a77-107">Définit la propriété **IdleTimeout** .</span><span class="sxs-lookup"><span data-stu-id="10a77-107">Sets the **IdleTimeout** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="10a77-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10a77-108">Syntax</span></span>


```mof
uint32 SetIdleTimeout(
  [in] uint32 IdleTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="10a77-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="10a77-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10a77-110">*IdleTimeout* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="10a77-110">*IdleTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10a77-111">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10a77-111">Type: **uint32**</span></span>

<span data-ttu-id="10a77-112">Nouvelle valeur du délai d’attente, en minutes.</span><span class="sxs-lookup"><span data-stu-id="10a77-112">The new timeout value, in minutes.</span></span> <span data-ttu-id="10a77-113">La valeur 0 signifie qu’il n’y a aucun délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="10a77-113">A value of 0 means there is no timeout.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10a77-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="10a77-114">Return value</span></span>

<span data-ttu-id="10a77-115">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10a77-115">Type: **uint32**</span></span>

<span data-ttu-id="10a77-116">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="10a77-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="10a77-117">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="10a77-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="10a77-118">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="10a77-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="10a77-119">Notes</span><span class="sxs-lookup"><span data-stu-id="10a77-119">Remarks</span></span>

<span data-ttu-id="10a77-120">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="10a77-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="10a77-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="10a77-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="10a77-122">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="10a77-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="10a77-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="10a77-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="10a77-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="10a77-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="10a77-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10a77-125">Requirements</span></span>



| <span data-ttu-id="10a77-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10a77-126">Requirement</span></span> | <span data-ttu-id="10a77-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="10a77-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="10a77-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10a77-128">Minimum supported client</span></span><br/> | <span data-ttu-id="10a77-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="10a77-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="10a77-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10a77-130">Minimum supported server</span></span><br/> | <span data-ttu-id="10a77-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="10a77-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="10a77-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="10a77-132">Namespace</span></span><br/>                | <span data-ttu-id="10a77-133">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="10a77-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="10a77-134">MOF</span><span class="sxs-lookup"><span data-stu-id="10a77-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10a77-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10a77-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="10a77-136">DLL</span><span class="sxs-lookup"><span data-stu-id="10a77-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10a77-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10a77-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="10a77-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10a77-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10a77-139">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="10a77-139">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

