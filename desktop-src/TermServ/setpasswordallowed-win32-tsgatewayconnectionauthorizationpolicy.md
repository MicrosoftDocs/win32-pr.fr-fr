---
title: Méthode SetPasswordAllowed de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Définit la propriété PasswordAllowed, qui active ou désactive la prise en charge de l’utilisation d’un mot de passe pour se connecter au serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: 2d2dfc45-ac2c-41dc-b2c1-4c8eab42c442
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetPasswordAllowed
- Services Bureau à distance de la méthode SetPasswordAllowed, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode SetPasswordAllowed
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetPasswordAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8bda5fde2fd79cc02697fd270fc307ef5f410f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385167"
---
# <a name="setpasswordallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="3a06d-106">Méthode SetPasswordAllowed de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="3a06d-106">SetPasswordAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="3a06d-107">Définit la propriété **PasswordAllowed** , qui active ou désactive la prise en charge de l’utilisation d’un mot de passe pour se connecter au serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="3a06d-107">Sets the **PasswordAllowed** property, which enables or disables support for using a password to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a06d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a06d-108">Syntax</span></span>


```mof
uint32 SetPasswordAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="3a06d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a06d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a06d-110">*Autorisé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3a06d-110">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a06d-111">Nouvelle valeur **PasswordAllowed** .</span><span class="sxs-lookup"><span data-stu-id="3a06d-111">New **PasswordAllowed** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a06d-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3a06d-112">Return value</span></span>

<span data-ttu-id="3a06d-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="3a06d-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3a06d-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="3a06d-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3a06d-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3a06d-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3a06d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="3a06d-116">Remarks</span></span>

<span data-ttu-id="3a06d-117">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3a06d-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="3a06d-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="3a06d-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3a06d-119">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3a06d-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3a06d-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="3a06d-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3a06d-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3a06d-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a06d-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a06d-122">Requirements</span></span>



| <span data-ttu-id="3a06d-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a06d-123">Requirement</span></span> | <span data-ttu-id="3a06d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a06d-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a06d-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a06d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3a06d-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a06d-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="3a06d-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a06d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3a06d-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a06d-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="3a06d-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3a06d-129">Namespace</span></span><br/>                | <span data-ttu-id="3a06d-130">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="3a06d-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="3a06d-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3a06d-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a06d-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a06d-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a06d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3a06d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a06d-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a06d-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3a06d-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a06d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a06d-136">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="3a06d-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

