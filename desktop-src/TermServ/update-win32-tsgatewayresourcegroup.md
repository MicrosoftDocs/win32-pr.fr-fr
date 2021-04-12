---
title: Méthode Update de la classe Win32_TSGatewayResourceGroup
description: Met à jour le groupe de ressources.
ms.assetid: b5927046-f461-41cd-861b-0fd77f2008e5
ms.tgt_platform: multiple
keywords:
- Mettre à jour la méthode Services Bureau à distance
- Mise à jour de la méthode Services Bureau à distance, classe Win32_TSGatewayResourceGroup
- Services Bureau à distance de la classe Win32_TSGatewayResourceGroup, méthode Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a7b1610fc14aa522fa4d8b7caf03fccd7b37375
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384759"
---
# <a name="update-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="c4d6f-106">Méthode Update de la \_ classe TSGatewayResourceGroup Win32</span><span class="sxs-lookup"><span data-stu-id="c4d6f-106">Update method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="c4d6f-107">Met à jour le groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="c4d6f-107">Updates the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4d6f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4d6f-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string Name,
  [in] string Description,
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="c4d6f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4d6f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4d6f-110">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4d6f-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4d6f-111">Nom du groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="c4d6f-111">Name of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="c4d6f-112">*Description* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4d6f-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4d6f-113">Description du groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="c4d6f-113">Description of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="c4d6f-114">*Ressources* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4d6f-114">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4d6f-115">Liste de ressources séparées par des points-virgules dans ce groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="c4d6f-115">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="c4d6f-116">« \* » Signifie toutes les ressources.</span><span class="sxs-lookup"><span data-stu-id="c4d6f-116">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4d6f-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4d6f-117">Return value</span></span>

<span data-ttu-id="c4d6f-118">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="c4d6f-118">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c4d6f-119">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="c4d6f-119">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c4d6f-120">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c4d6f-120">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c4d6f-121">Notes</span><span class="sxs-lookup"><span data-stu-id="c4d6f-121">Remarks</span></span>

<span data-ttu-id="c4d6f-122">Si plusieurs ressources sont dans le paramètre *Resources* et qu’une des ressources ne peut pas être traitée, aucune des ressources ne sera traitée.</span><span class="sxs-lookup"><span data-stu-id="c4d6f-122">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="c4d6f-123">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c4d6f-123">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c4d6f-124">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="c4d6f-124">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c4d6f-125">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c4d6f-125">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c4d6f-126">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="c4d6f-126">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c4d6f-127">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c4d6f-127">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4d6f-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4d6f-128">Requirements</span></span>



| <span data-ttu-id="c4d6f-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4d6f-129">Requirement</span></span> | <span data-ttu-id="c4d6f-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4d6f-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4d6f-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4d6f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c4d6f-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4d6f-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c4d6f-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4d6f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c4d6f-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4d6f-134">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c4d6f-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c4d6f-135">Namespace</span></span><br/>                | <span data-ttu-id="c4d6f-136">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="c4d6f-136">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c4d6f-137">MOF</span><span class="sxs-lookup"><span data-stu-id="c4d6f-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4d6f-138"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4d6f-138"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4d6f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c4d6f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4d6f-140"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4d6f-140"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c4d6f-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4d6f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4d6f-142">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="c4d6f-142">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

