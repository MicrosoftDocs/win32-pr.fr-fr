---
title: Méthode SetCookieAuthenticationAllowed de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Définit la propriété CookieAuthenticationAllowed.
ms.assetid: 481b89cb-d73b-4dae-941c-a629c2ae5ac4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetCookieAuthenticationAllowed
- Services Bureau à distance de la méthode SetCookieAuthenticationAllowed, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode SetCookieAuthenticationAllowed
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetCookieAuthenticationAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9293123ab6ce5b1ddcdb172f9258ba73b23fdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103153"
---
# <a name="setcookieauthenticationallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="e77ed-106">Méthode SetCookieAuthenticationAllowed de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="e77ed-106">SetCookieAuthenticationAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="e77ed-107">Définit la propriété **CookieAuthenticationAllowed** .</span><span class="sxs-lookup"><span data-stu-id="e77ed-107">Sets the **CookieAuthenticationAllowed** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="e77ed-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e77ed-108">Syntax</span></span>


```mof
uint32 SetCookieAuthenticationAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="e77ed-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e77ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e77ed-110">*Autorisé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e77ed-110">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e77ed-111">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e77ed-111">Type: **boolean**</span></span>

<span data-ttu-id="e77ed-112">Nouvelle valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="e77ed-112">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e77ed-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e77ed-113">Return value</span></span>

<span data-ttu-id="e77ed-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e77ed-114">Type: **uint32**</span></span>

<span data-ttu-id="e77ed-115">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="e77ed-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e77ed-116">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="e77ed-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e77ed-117">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e77ed-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e77ed-118">Notes</span><span class="sxs-lookup"><span data-stu-id="e77ed-118">Remarks</span></span>

<span data-ttu-id="e77ed-119">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="e77ed-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e77ed-120">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="e77ed-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e77ed-121">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e77ed-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e77ed-122">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="e77ed-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e77ed-123">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e77ed-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e77ed-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e77ed-124">Requirements</span></span>



| <span data-ttu-id="e77ed-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e77ed-125">Requirement</span></span> | <span data-ttu-id="e77ed-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="e77ed-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e77ed-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e77ed-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e77ed-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e77ed-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e77ed-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e77ed-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e77ed-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e77ed-130">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="e77ed-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e77ed-131">Namespace</span></span><br/>                | <span data-ttu-id="e77ed-132">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="e77ed-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e77ed-133">MOF</span><span class="sxs-lookup"><span data-stu-id="e77ed-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e77ed-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e77ed-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e77ed-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e77ed-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e77ed-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e77ed-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e77ed-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e77ed-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e77ed-138">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="e77ed-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

