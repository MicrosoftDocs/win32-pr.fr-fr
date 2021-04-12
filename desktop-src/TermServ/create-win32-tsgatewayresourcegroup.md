---
title: Créer une méthode de la classe Win32_TSGatewayResourceGroup
description: Crée un groupe de ressources.
ms.assetid: 715e6086-1c7d-4b20-983a-3ab98e875ca5
ms.tgt_platform: multiple
keywords:
- Créer une méthode Services Bureau à distance
- Create Method Services Bureau à distance, Win32_TSGatewayResourceGroup Class
- Win32_TSGatewayResourceGroup de la classe Services Bureau à distance, Create, méthode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9c5179967c143faa36763b7a2aabb8849d2f13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032524"
---
# <a name="create-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="20c54-106">Créer une méthode de la \_ classe TSGatewayResourceGroup Win32</span><span class="sxs-lookup"><span data-stu-id="20c54-106">Create method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="20c54-107">Crée un groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="20c54-107">Creates a resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="20c54-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20c54-108">Syntax</span></span>


```mof
uint32 Create(
  [in] string Name,
  [in] string Description,
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="20c54-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20c54-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20c54-110">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20c54-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20c54-111">Nom du groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="20c54-111">Name of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="20c54-112">*Description* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20c54-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20c54-113">Description du groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="20c54-113">Description of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="20c54-114">*Ressources* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20c54-114">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20c54-115">Liste de ressources séparées par des points-virgules dans ce groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="20c54-115">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="20c54-116">« \* » Signifie toutes les ressources.</span><span class="sxs-lookup"><span data-stu-id="20c54-116">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20c54-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20c54-117">Return value</span></span>

<span data-ttu-id="20c54-118">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="20c54-118">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="20c54-119">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="20c54-119">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="20c54-120">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="20c54-120">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="20c54-121">Notes</span><span class="sxs-lookup"><span data-stu-id="20c54-121">Remarks</span></span>

<span data-ttu-id="20c54-122">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="20c54-122">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="20c54-123">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="20c54-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="20c54-124">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="20c54-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="20c54-125">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="20c54-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="20c54-126">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="20c54-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="20c54-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20c54-127">Requirements</span></span>



| <span data-ttu-id="20c54-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20c54-128">Requirement</span></span> | <span data-ttu-id="20c54-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="20c54-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="20c54-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20c54-130">Minimum supported client</span></span><br/> | <span data-ttu-id="20c54-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="20c54-131">None supported</span></span><br/>                                                                |
| <span data-ttu-id="20c54-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20c54-132">Minimum supported server</span></span><br/> | <span data-ttu-id="20c54-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20c54-133">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="20c54-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="20c54-134">Namespace</span></span><br/>                | <span data-ttu-id="20c54-135">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="20c54-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="20c54-136">MOF</span><span class="sxs-lookup"><span data-stu-id="20c54-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20c54-137"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20c54-137"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="20c54-138">DLL</span><span class="sxs-lookup"><span data-stu-id="20c54-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20c54-139"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20c54-139"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="20c54-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20c54-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20c54-141">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="20c54-141">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

