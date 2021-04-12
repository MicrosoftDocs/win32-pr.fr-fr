---
title: Méthode RemoveResources de la classe Win32_TSGatewayResourceGroup
description: Supprime les ressources du groupe de ressources.
ms.assetid: 5f339990-8273-4658-843e-b6b7a85808e1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RemoveResources
- Services Bureau à distance de la méthode RemoveResources, classe Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup de la classe Services Bureau à distance, méthode RemoveResources
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.RemoveResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e3d1cc1e39d8c96833fc6a371741493457a28b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385259"
---
# <a name="removeresources-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="c45d7-106">Méthode RemoveResources de la \_ classe Win32 TSGatewayResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c45d7-106">RemoveResources method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="c45d7-107">Supprime les ressources du groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="c45d7-107">Removes resources from the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="c45d7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c45d7-108">Syntax</span></span>


```mof
uint32 RemoveResources(
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="c45d7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c45d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c45d7-110">*Ressources* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c45d7-110">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c45d7-111">Liste de ressources séparées par des points-virgules à supprimer.</span><span class="sxs-lookup"><span data-stu-id="c45d7-111">Semicolon-separated list of resources to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c45d7-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c45d7-112">Return value</span></span>

<span data-ttu-id="c45d7-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="c45d7-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c45d7-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="c45d7-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c45d7-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c45d7-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c45d7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c45d7-116">Remarks</span></span>

<span data-ttu-id="c45d7-117">Si plusieurs ressources sont dans le paramètre *Resources* et qu’une des ressources ne peut pas être traitée, aucune des ressources ne sera traitée.</span><span class="sxs-lookup"><span data-stu-id="c45d7-117">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="c45d7-118">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c45d7-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c45d7-119">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="c45d7-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c45d7-120">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c45d7-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c45d7-121">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="c45d7-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c45d7-122">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c45d7-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c45d7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c45d7-123">Requirements</span></span>



| <span data-ttu-id="c45d7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c45d7-124">Requirement</span></span> | <span data-ttu-id="c45d7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="c45d7-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c45d7-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c45d7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c45d7-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c45d7-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c45d7-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c45d7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c45d7-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c45d7-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c45d7-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c45d7-130">Namespace</span></span><br/>                | <span data-ttu-id="c45d7-131">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="c45d7-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c45d7-132">MOF</span><span class="sxs-lookup"><span data-stu-id="c45d7-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c45d7-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c45d7-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c45d7-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c45d7-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c45d7-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c45d7-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c45d7-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c45d7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c45d7-137">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="c45d7-137">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

