---
title: Méthode Delete de la classe Win32_TSGatewayResourceGroup
description: Supprime le groupe de ressources.
ms.assetid: 669a24b1-4828-498d-b249-7e9725d9bf72
ms.tgt_platform: multiple
keywords:
- Supprimer la méthode Services Bureau à distance
- Delete, méthode Services Bureau à distance, classe Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup de la classe Services Bureau à distance, méthode Delete
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.Delete
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d9123b7f63238cdb2007ecea49aaf0bca236a7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103093"
---
# <a name="delete-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="7c92a-106">Méthode Delete de la \_ classe TSGatewayResourceGroup Win32</span><span class="sxs-lookup"><span data-stu-id="7c92a-106">Delete method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="7c92a-107">Supprime le groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="7c92a-107">Deletes the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c92a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c92a-108">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="7c92a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c92a-109">Parameters</span></span>

<span data-ttu-id="7c92a-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7c92a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c92a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7c92a-111">Return value</span></span>

<span data-ttu-id="7c92a-112">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="7c92a-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="7c92a-113">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="7c92a-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="7c92a-114">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7c92a-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7c92a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="7c92a-115">Remarks</span></span>

<span data-ttu-id="7c92a-116">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="7c92a-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="7c92a-117">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="7c92a-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7c92a-118">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7c92a-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7c92a-119">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="7c92a-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7c92a-120">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7c92a-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c92a-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c92a-121">Requirements</span></span>



| <span data-ttu-id="7c92a-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c92a-122">Requirement</span></span> | <span data-ttu-id="7c92a-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c92a-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c92a-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c92a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7c92a-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c92a-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="7c92a-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c92a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7c92a-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c92a-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="7c92a-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7c92a-128">Namespace</span></span><br/>                | <span data-ttu-id="7c92a-129">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="7c92a-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="7c92a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="7c92a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c92a-131"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c92a-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c92a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7c92a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c92a-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c92a-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="7c92a-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c92a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c92a-135">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="7c92a-135">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

