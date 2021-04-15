---
title: Méthode AddResources de la classe Win32_TSGatewayResourceGroup
description: Ajoute des ressources au groupe de ressources.
ms.assetid: 3210b468-6b82-4edb-ac8b-95f66a7b9328
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AddResources
- Services Bureau à distance de la méthode AddResources, classe Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup de la classe Services Bureau à distance, méthode AddResources
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.AddResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a37498accf76b28f16e0de45565916c18ab8d9dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508365"
---
# <a name="addresources-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="eaf6d-106">Méthode AddResources de la \_ classe Win32 TSGatewayResourceGroup</span><span class="sxs-lookup"><span data-stu-id="eaf6d-106">AddResources method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="eaf6d-107">Ajoute des ressources au groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="eaf6d-107">Adds resources to the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaf6d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eaf6d-108">Syntax</span></span>


```mof
uint32 AddResources(
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="eaf6d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eaf6d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaf6d-110">*Ressources* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eaf6d-110">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eaf6d-111">Liste de ressources séparées par des points-virgules à ajouter au groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="eaf6d-111">Semicolon-separated list of resources to be added to the resource group.</span></span> <span data-ttu-id="eaf6d-112">« \* » Signifie toutes les ressources.</span><span class="sxs-lookup"><span data-stu-id="eaf6d-112">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaf6d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eaf6d-113">Return value</span></span>

<span data-ttu-id="eaf6d-114">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="eaf6d-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="eaf6d-115">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="eaf6d-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="eaf6d-116">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="eaf6d-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eaf6d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="eaf6d-117">Remarks</span></span>

<span data-ttu-id="eaf6d-118">Si plusieurs ressources sont dans le paramètre *Resources* et qu’une des ressources ne peut pas être traitée, aucune des ressources ne sera traitée.</span><span class="sxs-lookup"><span data-stu-id="eaf6d-118">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="eaf6d-119">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="eaf6d-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="eaf6d-120">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="eaf6d-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="eaf6d-121">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="eaf6d-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="eaf6d-122">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="eaf6d-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="eaf6d-123">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="eaf6d-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="eaf6d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eaf6d-124">Requirements</span></span>



| <span data-ttu-id="eaf6d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eaf6d-125">Requirement</span></span> | <span data-ttu-id="eaf6d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="eaf6d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf6d-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eaf6d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="eaf6d-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="eaf6d-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="eaf6d-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eaf6d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="eaf6d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eaf6d-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="eaf6d-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="eaf6d-131">Namespace</span></span><br/>                | <span data-ttu-id="eaf6d-132">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="eaf6d-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="eaf6d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="eaf6d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eaf6d-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eaf6d-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="eaf6d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="eaf6d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaf6d-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eaf6d-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="eaf6d-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eaf6d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaf6d-138">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="eaf6d-138">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

