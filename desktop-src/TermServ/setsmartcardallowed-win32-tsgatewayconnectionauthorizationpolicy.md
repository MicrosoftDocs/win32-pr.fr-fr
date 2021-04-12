---
title: Méthode SetSmartcardAllowed de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Définit la propriété SmartcardAllowed, qui active ou désactive la prise en charge de l’utilisation d’une carte à puce pour se connecter au serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: 9fe1c7a9-2bab-439f-8dc2-421ed876fcf7
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetSmartcardAllowed
- Services Bureau à distance de la méthode SetSmartcardAllowed, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode SetSmartcardAllowed
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSmartcardAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022b5461086ae05f198cbce4faaee0e9c36bf77e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384964"
---
# <a name="setsmartcardallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="95556-106">Méthode SetSmartcardAllowed de la \_ classe Win32 TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="95556-106">SetSmartcardAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="95556-107">Définit la propriété **SmartcardAllowed** , qui active ou désactive la prise en charge de l’utilisation d’une carte à puce pour se connecter au serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="95556-107">Sets the **SmartcardAllowed** property, which enables or disables support for using a smart card to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="95556-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95556-108">Syntax</span></span>


```mof
uint32 SetSmartcardAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="95556-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95556-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95556-110">*Autorisé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="95556-110">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95556-111">Nouvelle valeur **SmartcardAllowed** .</span><span class="sxs-lookup"><span data-stu-id="95556-111">New **SmartcardAllowed** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95556-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95556-112">Return value</span></span>

<span data-ttu-id="95556-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="95556-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="95556-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="95556-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="95556-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="95556-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="95556-116">Notes</span><span class="sxs-lookup"><span data-stu-id="95556-116">Remarks</span></span>

<span data-ttu-id="95556-117">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="95556-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="95556-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="95556-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="95556-119">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="95556-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="95556-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="95556-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="95556-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="95556-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="95556-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95556-122">Requirements</span></span>



| <span data-ttu-id="95556-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95556-123">Requirement</span></span> | <span data-ttu-id="95556-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="95556-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="95556-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95556-125">Minimum supported client</span></span><br/> | <span data-ttu-id="95556-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="95556-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="95556-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95556-127">Minimum supported server</span></span><br/> | <span data-ttu-id="95556-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95556-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="95556-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="95556-129">Namespace</span></span><br/>                | <span data-ttu-id="95556-130">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="95556-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="95556-131">MOF</span><span class="sxs-lookup"><span data-stu-id="95556-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95556-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95556-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="95556-133">DLL</span><span class="sxs-lookup"><span data-stu-id="95556-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95556-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95556-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="95556-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95556-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95556-136">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="95556-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

