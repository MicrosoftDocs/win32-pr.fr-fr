---
title: Méthode RemoveLSfromTSLSGroup de la classe Win32_TSLicenseServer
description: Supprime le Bureau à distance serveur de licences du groupe serveurs de licences Services Bureau à distance sur un contrôleur de domaine dans le même domaine que le serveur de licences.
ms.assetid: 5ed4595b-0668-4dd8-953e-b6fc61088cfd
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RemoveLSfromTSLSGroup
- Services Bureau à distance de la méthode RemoveLSfromTSLSGroup, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode RemoveLSfromTSLSGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.RemoveLSfromTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b60c7a0e6b836b8fcf268942ba5d8eae1304b818
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508742"
---
# <a name="removelsfromtslsgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="e405e-106">Méthode RemoveLSfromTSLSGroup de la \_ classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="e405e-106">RemoveLSfromTSLSGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="e405e-107">Supprime le Bureau à distance serveur de licences du groupe serveurs de licences Services Bureau à distance sur un contrôleur de domaine dans le même domaine que le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="e405e-107">Removes the Remote Desktop license server from the Remote Desktop Services License Servers group on a domain controller in the same domain as the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="e405e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e405e-108">Syntax</span></span>


```mof
uint32 RemoveLSfromTSLSGroup();
```



## <a name="parameters"></a><span data-ttu-id="e405e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e405e-109">Parameters</span></span>

<span data-ttu-id="e405e-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e405e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e405e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e405e-111">Return value</span></span>

<span data-ttu-id="e405e-112">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="e405e-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e405e-113">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="e405e-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e405e-114">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e405e-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e405e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e405e-115">Remarks</span></span>

<span data-ttu-id="e405e-116">Vous devez être membre du groupe Admins du domaine pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="e405e-116">You must be a member of the Domain Admins group to call this method.</span></span>

<span data-ttu-id="e405e-117">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="e405e-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e405e-118">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e405e-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e405e-119">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="e405e-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e405e-120">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e405e-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e405e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e405e-121">Requirements</span></span>



| <span data-ttu-id="e405e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e405e-122">Requirement</span></span> | <span data-ttu-id="e405e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e405e-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e405e-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e405e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e405e-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e405e-125">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="e405e-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e405e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e405e-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e405e-127">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="e405e-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e405e-128">Namespace</span></span><br/>                | <span data-ttu-id="e405e-129">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="e405e-129">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="e405e-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e405e-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e405e-131"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e405e-131"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e405e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e405e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e405e-133"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e405e-133"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e405e-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e405e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e405e-135">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="e405e-135">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

