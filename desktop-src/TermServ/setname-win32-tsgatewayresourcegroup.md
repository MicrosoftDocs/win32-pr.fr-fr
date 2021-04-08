---
title: Méthode SetName de la classe Win32_TSGatewayResourceGroup
description: Définit la propriété de nom du groupe de ressources.
ms.assetid: 2c2fe1b6-5826-490e-aec2-479a0191e215
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetName
- Services Bureau à distance de la méthode SetName, classe Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup de la classe Services Bureau à distance, méthode SetName
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac9ea16eb82896bb8fad67fff7ed849308100726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843581"
---
# <a name="setname-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="9be51-106">Méthode SetName de la \_ classe Win32 TSGatewayResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9be51-106">SetName method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="9be51-107">Définit la propriété de **nom** du groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="9be51-107">Sets the **Name** property for the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="9be51-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9be51-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="9be51-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9be51-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9be51-110">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9be51-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9be51-111">Nom du groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="9be51-111">Name of the resource group.</span></span> <span data-ttu-id="9be51-112">Le nom doit comporter 64 caractères ou moins, unique (la casse est ignorée) et ne peut pas contenir les caractères réservés suivants :</span><span class="sxs-lookup"><span data-stu-id="9be51-112">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="9be51-113"><>  :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="9be51-113"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="9be51-114">\*\[Onglet\]</span><span class="sxs-lookup"><span data-stu-id="9be51-114">\* \[TAB\]</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9be51-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9be51-115">Return value</span></span>

<span data-ttu-id="9be51-116">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="9be51-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="9be51-117">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="9be51-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="9be51-118">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9be51-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9be51-119">Notes</span><span class="sxs-lookup"><span data-stu-id="9be51-119">Remarks</span></span>

<span data-ttu-id="9be51-120">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="9be51-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="9be51-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="9be51-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9be51-122">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9be51-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9be51-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="9be51-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9be51-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9be51-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9be51-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9be51-125">Requirements</span></span>



| <span data-ttu-id="9be51-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9be51-126">Requirement</span></span> | <span data-ttu-id="9be51-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="9be51-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9be51-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9be51-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9be51-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9be51-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9be51-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9be51-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9be51-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9be51-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9be51-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9be51-132">Namespace</span></span><br/>                | <span data-ttu-id="9be51-133">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="9be51-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="9be51-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9be51-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9be51-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9be51-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="9be51-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9be51-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9be51-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9be51-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9be51-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9be51-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9be51-139">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="9be51-139">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

