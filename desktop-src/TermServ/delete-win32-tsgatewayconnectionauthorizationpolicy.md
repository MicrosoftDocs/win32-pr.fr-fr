---
title: Méthode Delete de la classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Supprime la stratégie d’autorisation de connexion Bureau à distance actuelle (RD \ 160 ; CAP).
ms.assetid: aef7216a-4459-492b-95cb-87ea760dcde9
ms.tgt_platform: multiple
keywords:
- Supprimer la méthode Services Bureau à distance
- Delete, méthode Services Bureau à distance, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de la classe Services Bureau à distance, méthode Delete
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Delete
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26b99cf7856c31f2e45f026631beb974e61c481f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510521"
---
# <a name="delete-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="44c35-106">Méthode Delete de la \_ classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="44c35-106">Delete method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="44c35-107">Supprime la stratégie d’autorisation des connexions Bureau à distance en cours.</span><span class="sxs-lookup"><span data-stu-id="44c35-107">Deletes the current Remote Desktop connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="44c35-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44c35-108">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="44c35-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44c35-109">Parameters</span></span>

<span data-ttu-id="44c35-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="44c35-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44c35-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="44c35-111">Return value</span></span>

<span data-ttu-id="44c35-112">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="44c35-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="44c35-113">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="44c35-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="44c35-114">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="44c35-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="44c35-115">Notes</span><span class="sxs-lookup"><span data-stu-id="44c35-115">Remarks</span></span>

<span data-ttu-id="44c35-116">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="44c35-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="44c35-117">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="44c35-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="44c35-118">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="44c35-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="44c35-119">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="44c35-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="44c35-120">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="44c35-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="44c35-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44c35-121">Requirements</span></span>



| <span data-ttu-id="44c35-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44c35-122">Requirement</span></span> | <span data-ttu-id="44c35-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="44c35-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="44c35-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44c35-124">Minimum supported client</span></span><br/> | <span data-ttu-id="44c35-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="44c35-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="44c35-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44c35-126">Minimum supported server</span></span><br/> | <span data-ttu-id="44c35-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44c35-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="44c35-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="44c35-128">Namespace</span></span><br/>                | <span data-ttu-id="44c35-129">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="44c35-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="44c35-130">MOF</span><span class="sxs-lookup"><span data-stu-id="44c35-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44c35-131"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44c35-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="44c35-132">DLL</span><span class="sxs-lookup"><span data-stu-id="44c35-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44c35-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44c35-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="44c35-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44c35-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44c35-135">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="44c35-135">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

