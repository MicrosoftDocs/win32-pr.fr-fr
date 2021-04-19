---
title: Méthode SetDescription de la classe Win32_TSGatewayResourceGroup
description: Définit la propriété Description du groupe de ressources.
ms.assetid: ab1280c7-ce53-4807-9537-953b597dd636
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetDescription
- Services Bureau à distance de la méthode SetDescription, classe Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup de la classe Services Bureau à distance, méthode SetDescription
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetDescription
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d815cc5400a182f2dff3b982643d5e6bfd861002
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511398"
---
# <a name="setdescription-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="04e12-106">Méthode SetDescription de la \_ classe Win32 TSGatewayResourceGroup</span><span class="sxs-lookup"><span data-stu-id="04e12-106">SetDescription method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="04e12-107">Définit la propriété **Description** du groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="04e12-107">Sets the **Description** property for the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="04e12-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04e12-108">Syntax</span></span>


```mof
uint32 SetDescription(
  [in] string Description
);
```



## <a name="parameters"></a><span data-ttu-id="04e12-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04e12-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04e12-110">*Description* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="04e12-110">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04e12-111">Description du groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="04e12-111">Description of the resource group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04e12-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="04e12-112">Return value</span></span>

<span data-ttu-id="04e12-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="04e12-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="04e12-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="04e12-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="04e12-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="04e12-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="04e12-116">Notes</span><span class="sxs-lookup"><span data-stu-id="04e12-116">Remarks</span></span>

<span data-ttu-id="04e12-117">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="04e12-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="04e12-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="04e12-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="04e12-119">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="04e12-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="04e12-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="04e12-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="04e12-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="04e12-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="04e12-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04e12-122">Requirements</span></span>



| <span data-ttu-id="04e12-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04e12-123">Requirement</span></span> | <span data-ttu-id="04e12-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="04e12-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="04e12-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04e12-125">Minimum supported client</span></span><br/> | <span data-ttu-id="04e12-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="04e12-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="04e12-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04e12-127">Minimum supported server</span></span><br/> | <span data-ttu-id="04e12-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04e12-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="04e12-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="04e12-129">Namespace</span></span><br/>                | <span data-ttu-id="04e12-130">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="04e12-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="04e12-131">MOF</span><span class="sxs-lookup"><span data-stu-id="04e12-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04e12-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04e12-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="04e12-133">DLL</span><span class="sxs-lookup"><span data-stu-id="04e12-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04e12-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04e12-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="04e12-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04e12-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04e12-136">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="04e12-136">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

