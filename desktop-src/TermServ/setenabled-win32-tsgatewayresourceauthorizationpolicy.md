---
title: Méthode SetEnabled de la classe Win32_TSGatewayResourceAuthorizationPolicy
description: Active ou désactive la stratégie d’autorisation d’accès aux ressources Bureau à distance (RD \ 160 ; RAP) en définissant la propriété activé.
ms.assetid: ee5830ba-36a1-4f28-a902-be5867439ada
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetEnabled
- Services Bureau à distance de la méthode SetEnabled, classe Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy de la classe Services Bureau à distance, méthode SetEnabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de7c4e013690a5d5e8ffd6b235a42ea43c445ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466738"
---
# <a name="setenabled-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="66239-106">Méthode SetEnabled de la \_ classe Win32 TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="66239-106">SetEnabled method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="66239-107">Active ou désactive la stratégie d’autorisation des ressources Bureau à distance (RD RAP) en définissant la propriété **Enabled** .</span><span class="sxs-lookup"><span data-stu-id="66239-107">Enables or disables the Remote Desktop resource authorization policy (RD RAP) by setting the **Enabled** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="66239-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66239-108">Syntax</span></span>


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="66239-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66239-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66239-110">*Activé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="66239-110">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66239-111">Si la **valeur est true**, le rap des services Bureau à distance est activé.</span><span class="sxs-lookup"><span data-stu-id="66239-111">If **True**, the RD RAP will be enabled.</span></span> <span data-ttu-id="66239-112">Si la **valeur est false**, la valeur RD RAP est désactivée.</span><span class="sxs-lookup"><span data-stu-id="66239-112">If **False**, the RD RAP will be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66239-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="66239-113">Return value</span></span>

<span data-ttu-id="66239-114">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="66239-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="66239-115">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="66239-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="66239-116">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="66239-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="66239-117">Notes</span><span class="sxs-lookup"><span data-stu-id="66239-117">Remarks</span></span>

<span data-ttu-id="66239-118">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="66239-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="66239-119">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="66239-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="66239-120">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="66239-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="66239-121">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="66239-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="66239-122">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="66239-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="66239-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66239-123">Requirements</span></span>



| <span data-ttu-id="66239-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66239-124">Requirement</span></span> | <span data-ttu-id="66239-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="66239-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="66239-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66239-126">Minimum supported client</span></span><br/> | <span data-ttu-id="66239-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="66239-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="66239-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66239-128">Minimum supported server</span></span><br/> | <span data-ttu-id="66239-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66239-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="66239-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="66239-130">Namespace</span></span><br/>                | <span data-ttu-id="66239-131">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="66239-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="66239-132">MOF</span><span class="sxs-lookup"><span data-stu-id="66239-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66239-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66239-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="66239-134">DLL</span><span class="sxs-lookup"><span data-stu-id="66239-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66239-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66239-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="66239-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66239-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66239-137">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="66239-137">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

