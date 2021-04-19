---
title: Méthode EnableRequestSOH de la classe Win32_TSGatewayServerSettings
description: EnableRequestSOH n’est plus disponible.
ms.assetid: 4feb7530-cced-4ead-a1fb-679b81442bb3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode EnableRequestSOH
- Services Bureau à distance de la méthode EnableRequestSOH, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode EnableRequestSOH
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableRequestSOH
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90ed6a3929b50d13a27ec559aab534f9e06f738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510776"
---
# <a name="enablerequestsoh-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="d3ab1-106">Méthode EnableRequestSOH de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="d3ab1-106">EnableRequestSOH method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="d3ab1-107">\[La méthode **EnableRequestSOH** n’est plus disponible à partir de Windows Server 2016.\]</span><span class="sxs-lookup"><span data-stu-id="d3ab1-107">\[The **EnableRequestSOH** method is no longer available as of Windows Server 2016.\]</span></span>

<span data-ttu-id="d3ab1-108">Active ou désactive les demandes pour une déclaration d’intégrité (SoH).</span><span class="sxs-lookup"><span data-stu-id="d3ab1-108">Enables or disables requests for a Statement of Health (SoH).</span></span>

## <a name="syntax"></a><span data-ttu-id="d3ab1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3ab1-109">Syntax</span></span>


```mof
uint32 EnableRequestSOH(
  [in] boolean RequestSOH
);
```



## <a name="parameters"></a><span data-ttu-id="d3ab1-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3ab1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3ab1-111">*RequestSOH* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d3ab1-111">*RequestSOH* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3ab1-112">Spécifiez **true** pour activer la fonctionnalité ou **false** pour la désactiver.</span><span class="sxs-lookup"><span data-stu-id="d3ab1-112">Specify **TRUE** to enable the feature or **FALSE** to disable the feature.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3ab1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d3ab1-113">Return value</span></span>

<span data-ttu-id="d3ab1-114">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="d3ab1-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d3ab1-115">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="d3ab1-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d3ab1-116">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d3ab1-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d3ab1-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d3ab1-117">Remarks</span></span>

<span data-ttu-id="d3ab1-118">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="d3ab1-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d3ab1-119">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="d3ab1-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d3ab1-120">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d3ab1-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d3ab1-121">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="d3ab1-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d3ab1-122">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d3ab1-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3ab1-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3ab1-123">Requirements</span></span>



| <span data-ttu-id="d3ab1-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3ab1-124">Requirement</span></span> | <span data-ttu-id="d3ab1-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3ab1-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3ab1-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3ab1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d3ab1-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3ab1-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d3ab1-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3ab1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d3ab1-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3ab1-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d3ab1-130">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="d3ab1-130">End of server support</span></span><br/>    | <span data-ttu-id="d3ab1-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d3ab1-131">Windows Server 2012 R2</span></span><br/>                                                        |
| <span data-ttu-id="d3ab1-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d3ab1-132">Namespace</span></span><br/>                | <span data-ttu-id="d3ab1-133">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="d3ab1-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="d3ab1-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d3ab1-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3ab1-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3ab1-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3ab1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d3ab1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3ab1-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3ab1-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="d3ab1-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3ab1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3ab1-139">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="d3ab1-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

