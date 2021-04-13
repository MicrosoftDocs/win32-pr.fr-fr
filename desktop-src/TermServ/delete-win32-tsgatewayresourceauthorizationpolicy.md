---
title: Méthode Delete de la classe Win32_TSGatewayResourceAuthorizationPolicy
description: Supprime la stratégie d’autorisation d’accès aux ressources Bureau à distance en cours (RD \ 160 ; RAP).
ms.assetid: cbabb997-63b8-4a4c-9e16-34f2638fca97
ms.tgt_platform: multiple
keywords:
- Supprimer la méthode Services Bureau à distance
- Delete, méthode Services Bureau à distance, classe Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy de la classe Services Bureau à distance, méthode Delete
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Delete
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396a766fb307d1e8a912d614147a2bff2bd924c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384072"
---
# <a name="delete-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="5419b-106">Méthode Delete de la \_ classe TSGatewayResourceAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="5419b-106">Delete method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="5419b-107">Supprime la stratégie d’autorisation d’accès aux ressources Bureau à distance en cours (RD RAP).</span><span class="sxs-lookup"><span data-stu-id="5419b-107">Deletes the current Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="5419b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5419b-108">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="5419b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5419b-109">Parameters</span></span>

<span data-ttu-id="5419b-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5419b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5419b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5419b-111">Return value</span></span>

<span data-ttu-id="5419b-112">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="5419b-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5419b-113">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="5419b-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5419b-114">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5419b-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5419b-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5419b-115">Remarks</span></span>

<span data-ttu-id="5419b-116">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="5419b-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="5419b-117">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="5419b-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5419b-118">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5419b-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5419b-119">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="5419b-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5419b-120">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5419b-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5419b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5419b-121">Requirements</span></span>



| <span data-ttu-id="5419b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5419b-122">Requirement</span></span> | <span data-ttu-id="5419b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5419b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5419b-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5419b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5419b-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5419b-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5419b-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5419b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5419b-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5419b-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5419b-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5419b-128">Namespace</span></span><br/>                | <span data-ttu-id="5419b-129">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="5419b-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5419b-130">MOF</span><span class="sxs-lookup"><span data-stu-id="5419b-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5419b-131"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5419b-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="5419b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5419b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5419b-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5419b-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="5419b-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5419b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5419b-135">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="5419b-135">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

