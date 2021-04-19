---
title: Méthode SetSecureIdAllowed de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Cette méthode est réservée à une utilisation ultérieure.
ms.assetid: 9f49e69a-c004-4e3e-b238-69865e3bf00b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetSecureIdAllowed
- Services Bureau à distance de la méthode SetSecureIdAllowed, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode SetSecureIdAllowed
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSecureIdAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70e61c158a7dfcafb6d1d5ac66833e42284b818d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513802"
---
# <a name="setsecureidallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="c4a84-106">Méthode SetSecureIdAllowed de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="c4a84-106">SetSecureIdAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="c4a84-107">Cette méthode est réservée à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c4a84-107">This method is reserved for future use.</span></span>

<span data-ttu-id="c4a84-108">Définit la propriété **SecureIdAllowed** , qui est réservée à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c4a84-108">Sets the **SecureIdAllowed** property, which is reserved for future use.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4a84-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4a84-109">Syntax</span></span>


```mof
uint32 SetSecureIdAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="c4a84-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4a84-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4a84-111">*Autorisé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4a84-111">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4a84-112">Nouvelle valeur **SecureIdAllowed** .</span><span class="sxs-lookup"><span data-stu-id="c4a84-112">New **SecureIdAllowed** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4a84-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4a84-113">Return value</span></span>

<span data-ttu-id="c4a84-114">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="c4a84-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c4a84-115">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="c4a84-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c4a84-116">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c4a84-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c4a84-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c4a84-117">Remarks</span></span>

<span data-ttu-id="c4a84-118">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c4a84-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c4a84-119">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="c4a84-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c4a84-120">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c4a84-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c4a84-121">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="c4a84-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c4a84-122">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c4a84-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4a84-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4a84-123">Requirements</span></span>



| <span data-ttu-id="c4a84-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4a84-124">Requirement</span></span> | <span data-ttu-id="c4a84-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4a84-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4a84-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4a84-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c4a84-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4a84-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c4a84-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4a84-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c4a84-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4a84-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c4a84-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c4a84-130">Namespace</span></span><br/>                | <span data-ttu-id="c4a84-131">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="c4a84-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c4a84-132">MOF</span><span class="sxs-lookup"><span data-stu-id="c4a84-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4a84-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4a84-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4a84-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c4a84-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4a84-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4a84-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c4a84-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4a84-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4a84-137">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="c4a84-137">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

