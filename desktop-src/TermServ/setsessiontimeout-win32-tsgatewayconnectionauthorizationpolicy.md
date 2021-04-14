---
title: Méthode SetSessionTimeout de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Définit les propriétés SessionTimeout et SessionTimeoutAction.
ms.assetid: 11491c97-3ef8-46c1-9504-696c613e374e
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetSessionTimeout
- Services Bureau à distance de la méthode SetSessionTimeout, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode SetSessionTimeout
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSessionTimeout
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e544b59ae4fe0b74d0c120e6884ab81743cac6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508830"
---
# <a name="setsessiontimeout-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="e1574-106">Méthode SetSessionTimeout de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="e1574-106">SetSessionTimeout method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="e1574-107">Définit les propriétés **SessionTimeout** et **SessionTimeoutAction** .</span><span class="sxs-lookup"><span data-stu-id="e1574-107">Sets the **SessionTimeout** and **SessionTimeoutAction** properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1574-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1574-108">Syntax</span></span>


```mof
uint32 SetSessionTimeout(
  [in] uint32 SessionTimeout,
  [in] uint32 SessionTimeoutAction
);
```



## <a name="parameters"></a><span data-ttu-id="e1574-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1574-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1574-110">*SessionTimeout* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1574-110">*SessionTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1574-111">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e1574-111">Type: **uint32**</span></span>

<span data-ttu-id="e1574-112">Nouvelle valeur du délai d’attente, en minutes.</span><span class="sxs-lookup"><span data-stu-id="e1574-112">The new timeout value, in minutes.</span></span> <span data-ttu-id="e1574-113">La valeur 0 signifie qu’il n’y a aucun délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="e1574-113">A value of 0 means there is no timeout.</span></span>

</dd> <dt>

<span data-ttu-id="e1574-114">*SessionTimeoutAction* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1574-114">*SessionTimeoutAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1574-115">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e1574-115">Type: **uint32**</span></span>

<span data-ttu-id="e1574-116">Spécifie l’action à entreprendre en cas de délai d’expiration de session.</span><span class="sxs-lookup"><span data-stu-id="e1574-116">Specifies the action to be taken in case of a session timeout.</span></span> <span data-ttu-id="e1574-117">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e1574-117">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="e1574-118">0</span><span class="sxs-lookup"><span data-stu-id="e1574-118">0</span></span>
</dt> <dd>

<span data-ttu-id="e1574-119">Déconnectez la session.</span><span class="sxs-lookup"><span data-stu-id="e1574-119">Disconnect the session.</span></span>

</dd> <dt>

<span data-ttu-id="e1574-120">1</span><span class="sxs-lookup"><span data-stu-id="e1574-120">1</span></span>
</dt> <dd>

<span data-ttu-id="e1574-121">Essayez de réautoriser la session.</span><span class="sxs-lookup"><span data-stu-id="e1574-121">Attempt to re-authorize the session.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1574-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1574-122">Return value</span></span>

<span data-ttu-id="e1574-123">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e1574-123">Type: **uint32**</span></span>

<span data-ttu-id="e1574-124">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="e1574-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e1574-125">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="e1574-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e1574-126">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e1574-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e1574-127">Notes</span><span class="sxs-lookup"><span data-stu-id="e1574-127">Remarks</span></span>

<span data-ttu-id="e1574-128">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="e1574-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e1574-129">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="e1574-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e1574-130">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e1574-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e1574-131">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="e1574-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e1574-132">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e1574-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1574-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1574-133">Requirements</span></span>



| <span data-ttu-id="e1574-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1574-134">Requirement</span></span> | <span data-ttu-id="e1574-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1574-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1574-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1574-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e1574-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1574-137">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e1574-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1574-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e1574-139">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e1574-139">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="e1574-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e1574-140">Namespace</span></span><br/>                | <span data-ttu-id="e1574-141">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="e1574-141">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e1574-142">MOF</span><span class="sxs-lookup"><span data-stu-id="e1574-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1574-143"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1574-143"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1574-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e1574-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1574-145"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1574-145"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e1574-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1574-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1574-147">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="e1574-147">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

