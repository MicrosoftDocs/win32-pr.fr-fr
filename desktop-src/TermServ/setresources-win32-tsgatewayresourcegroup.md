---
title: Méthode SetResources de la classe Win32_TSGatewayResourceGroup
description: Définit la propriété des ressources pour ce groupe de ressources.
ms.assetid: 0043ee04-26d1-4907-87cc-a15f72cb0b93
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetResources
- Services Bureau à distance de la méthode SetResources, classe Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup de la classe Services Bureau à distance, méthode SetResources
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23f2ca14597fc7d6ce3660e6e180bf93dfd86cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384275"
---
# <a name="setresources-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="29767-106">Méthode SetResources de la \_ classe Win32 TSGatewayResourceGroup</span><span class="sxs-lookup"><span data-stu-id="29767-106">SetResources method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="29767-107">Définit la propriété des **ressources** pour ce groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="29767-107">Sets the **Resources** property for this resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="29767-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29767-108">Syntax</span></span>


```mof
uint32 SetResources(
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="29767-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29767-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29767-110">*Ressources* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="29767-110">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29767-111">Liste de ressources séparées par des points-virgules dans ce groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="29767-111">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="29767-112">« \* » Signifie toutes les ressources.</span><span class="sxs-lookup"><span data-stu-id="29767-112">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29767-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="29767-113">Return value</span></span>

<span data-ttu-id="29767-114">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="29767-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="29767-115">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="29767-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="29767-116">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="29767-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="29767-117">Notes</span><span class="sxs-lookup"><span data-stu-id="29767-117">Remarks</span></span>

<span data-ttu-id="29767-118">Si plusieurs ressources sont dans le paramètre *Resources* et qu’une des ressources ne peut pas être traitée, aucune des ressources ne sera traitée.</span><span class="sxs-lookup"><span data-stu-id="29767-118">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="29767-119">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="29767-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="29767-120">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="29767-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="29767-121">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="29767-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="29767-122">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="29767-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="29767-123">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="29767-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="29767-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29767-124">Requirements</span></span>



| <span data-ttu-id="29767-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29767-125">Requirement</span></span> | <span data-ttu-id="29767-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="29767-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="29767-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29767-127">Minimum supported client</span></span><br/> | <span data-ttu-id="29767-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="29767-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="29767-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29767-129">Minimum supported server</span></span><br/> | <span data-ttu-id="29767-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29767-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="29767-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="29767-131">Namespace</span></span><br/>                | <span data-ttu-id="29767-132">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="29767-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="29767-133">MOF</span><span class="sxs-lookup"><span data-stu-id="29767-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29767-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29767-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="29767-135">DLL</span><span class="sxs-lookup"><span data-stu-id="29767-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29767-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29767-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="29767-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29767-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29767-138">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="29767-138">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

