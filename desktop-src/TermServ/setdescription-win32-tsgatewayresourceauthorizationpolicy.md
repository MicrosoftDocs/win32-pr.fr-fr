---
title: Méthode SetDescription de la classe Win32_TSGatewayResourceAuthorizationPolicy
description: Définit la propriété Description pour la stratégie d’autorisation d’accès aux ressources Bureau à distance (RD \ 160 ; RAP).
ms.assetid: 5a0f4c4b-50a4-4bd2-960f-8af7f4686d07
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetDescription
- Services Bureau à distance de la méthode SetDescription, classe Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy de la classe Services Bureau à distance, méthode SetDescription
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetDescription
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5dfdbcf67096dacc694061b5ff7e704c788bd2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384563"
---
# <a name="setdescription-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="584ea-106">Méthode SetDescription de la \_ classe Win32 TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="584ea-106">SetDescription method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="584ea-107">Définit la propriété **Description** de la stratégie d’autorisation des ressources Bureau À distance (RD RAP).</span><span class="sxs-lookup"><span data-stu-id="584ea-107">Sets the **Description** property for the Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="584ea-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="584ea-108">Syntax</span></span>


```mof
uint32 SetDescription(
  [in] string Description
);
```



## <a name="parameters"></a><span data-ttu-id="584ea-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="584ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="584ea-110">*Description* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="584ea-110">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="584ea-111">Description de la RD RAP.</span><span class="sxs-lookup"><span data-stu-id="584ea-111">Description of the RD RAP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="584ea-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="584ea-112">Return value</span></span>

<span data-ttu-id="584ea-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="584ea-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="584ea-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="584ea-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="584ea-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="584ea-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="584ea-116">Notes</span><span class="sxs-lookup"><span data-stu-id="584ea-116">Remarks</span></span>

<span data-ttu-id="584ea-117">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="584ea-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="584ea-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="584ea-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="584ea-119">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="584ea-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="584ea-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="584ea-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="584ea-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="584ea-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="584ea-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="584ea-122">Requirements</span></span>



| <span data-ttu-id="584ea-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="584ea-123">Requirement</span></span> | <span data-ttu-id="584ea-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="584ea-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="584ea-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="584ea-125">Minimum supported client</span></span><br/> | <span data-ttu-id="584ea-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="584ea-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="584ea-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="584ea-127">Minimum supported server</span></span><br/> | <span data-ttu-id="584ea-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="584ea-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="584ea-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="584ea-129">Namespace</span></span><br/>                | <span data-ttu-id="584ea-130">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="584ea-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="584ea-131">MOF</span><span class="sxs-lookup"><span data-stu-id="584ea-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="584ea-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="584ea-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="584ea-133">DLL</span><span class="sxs-lookup"><span data-stu-id="584ea-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="584ea-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="584ea-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="584ea-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="584ea-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="584ea-136">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="584ea-136">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

