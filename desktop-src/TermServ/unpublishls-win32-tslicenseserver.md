---
title: Méthode UnpublishLS de la classe Win32_TSLicenseServer
description: Annule la publication d’un serveur de licences Bureau à distance à partir de Active Directory Domain Services.
ms.assetid: 275854e2-85f6-4142-8bce-8d633bfcff7d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode UnpublishLS
- Services Bureau à distance de la méthode UnpublishLS, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode UnpublishLS
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.UnpublishLS
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1ec183b5be8055dc30add5bc00a7eb537cd20f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508733"
---
# <a name="unpublishls-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="fbf35-106">Méthode UnpublishLS de la \_ classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="fbf35-106">UnpublishLS method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="fbf35-107">Annule la publication d’un serveur de licences Bureau à distance à partir de Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="fbf35-107">Unpublishes a Remote Desktop license server from Active Directory Domain Services.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf35-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbf35-108">Syntax</span></span>


```mof
uint32 UnpublishLS();
```



## <a name="parameters"></a><span data-ttu-id="fbf35-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fbf35-109">Parameters</span></span>

<span data-ttu-id="fbf35-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="fbf35-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fbf35-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fbf35-111">Return value</span></span>

<span data-ttu-id="fbf35-112">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="fbf35-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="fbf35-113">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="fbf35-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="fbf35-114">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fbf35-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fbf35-115">Notes</span><span class="sxs-lookup"><span data-stu-id="fbf35-115">Remarks</span></span>

<span data-ttu-id="fbf35-116">Pour appeler cette méthode, vous devez être connecté en tant qu’administrateur d’entreprise à la forêt dans laquelle le serveur de licences est membre.</span><span class="sxs-lookup"><span data-stu-id="fbf35-116">To call this method, you must be logged on as an enterprise administrator to the forest in which the license server is a member.</span></span>

<span data-ttu-id="fbf35-117">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="fbf35-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fbf35-118">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fbf35-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fbf35-119">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="fbf35-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fbf35-120">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fbf35-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fbf35-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbf35-121">Requirements</span></span>



| <span data-ttu-id="fbf35-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fbf35-122">Requirement</span></span> | <span data-ttu-id="fbf35-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbf35-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf35-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbf35-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf35-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbf35-125">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="fbf35-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbf35-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf35-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fbf35-127">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="fbf35-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fbf35-128">Namespace</span></span><br/>                | <span data-ttu-id="fbf35-129">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="fbf35-129">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="fbf35-130">MOF</span><span class="sxs-lookup"><span data-stu-id="fbf35-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbf35-131"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fbf35-131"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbf35-132">DLL</span><span class="sxs-lookup"><span data-stu-id="fbf35-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbf35-133"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbf35-133"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbf35-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbf35-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbf35-135">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="fbf35-135">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

