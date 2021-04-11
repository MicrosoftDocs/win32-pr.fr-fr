---
title: Méthode EnableCentralCAP de la classe Win32_TSGatewayServerSettings
description: Contrôle la propriété CentralCAPEnabled, qui contrôle les stratégies d’autorisation de connexion Services Bureau à distance (RD \ 160 ; Cap) pour le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: 43e476df-714d-43bd-b40f-33511b7757a4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode EnableCentralCAP
- Services Bureau à distance de la méthode EnableCentralCAP, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode EnableCentralCAP
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableCentralCAP
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 933e91a89f9a5afdcd2ae85fa6cb097ef0c29cd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385292"
---
# <a name="enablecentralcap-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="e77f0-106">Méthode EnableCentralCAP de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="e77f0-106">EnableCentralCAP method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="e77f0-107">Contrôle la propriété **CentralCAPEnabled** , qui contrôle le services Bureau à distance les stratégies d’autorisation des connexions aux services Bureau à distance pour le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="e77f0-107">Controls the **CentralCAPEnabled** property, which controls the Remote Desktop Services connection authorization policies (RD CAPs) for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="e77f0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e77f0-108">Syntax</span></span>


```mof
uint32 EnableCentralCAP(
  [in] boolean CentralCAPEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="e77f0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e77f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e77f0-110">*CentralCAPEnabled* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e77f0-110">*CentralCAPEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e77f0-111">Si la valeur est **true**, les connexions Bureau à distance des serveurs de la stratégie d’autorisation des connexions aux services Bureau à distance sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="e77f0-111">If set to **True**, RD CAPs from central RD CAP servers will be used.</span></span> <span data-ttu-id="e77f0-112">Si la valeur est **false**, seules les stratégies du serveur local sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="e77f0-112">If set to **False**, only policies from the local server will be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e77f0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e77f0-113">Return value</span></span>

<span data-ttu-id="e77f0-114">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="e77f0-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e77f0-115">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="e77f0-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e77f0-116">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e77f0-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e77f0-117">Notes</span><span class="sxs-lookup"><span data-stu-id="e77f0-117">Remarks</span></span>

<span data-ttu-id="e77f0-118">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="e77f0-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e77f0-119">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="e77f0-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e77f0-120">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e77f0-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e77f0-121">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="e77f0-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e77f0-122">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e77f0-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e77f0-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e77f0-123">Requirements</span></span>



| <span data-ttu-id="e77f0-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e77f0-124">Requirement</span></span> | <span data-ttu-id="e77f0-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e77f0-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e77f0-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e77f0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e77f0-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e77f0-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e77f0-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e77f0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e77f0-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e77f0-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e77f0-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e77f0-130">Namespace</span></span><br/>                | <span data-ttu-id="e77f0-131">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="e77f0-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e77f0-132">MOF</span><span class="sxs-lookup"><span data-stu-id="e77f0-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e77f0-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e77f0-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e77f0-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e77f0-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e77f0-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e77f0-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e77f0-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e77f0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e77f0-137">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="e77f0-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

