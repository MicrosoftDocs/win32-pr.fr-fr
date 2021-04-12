---
title: Méthode GetLicenseServerId de la classe Win32_TSLicenseServer
description: Récupère le Bureau à distance identificateur du serveur de licences si le serveur est actuellement activé.
ms.assetid: 0eb2cf82-3632-4693-97d2-0cfa814d8c94
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetLicenseServerId
- Services Bureau à distance de la méthode GetLicenseServerId, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode GetLicenseServerId
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.GetLicenseServerId
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43a5883a5a52a0d111959e1f9fc1cbe9da5357d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384328"
---
# <a name="getlicenseserverid-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="62768-106">Méthode GetLicenseServerId de la \_ classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="62768-106">GetLicenseServerId method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="62768-107">Récupère le Bureau à distance identificateur du serveur de licences si le serveur est actuellement activé.</span><span class="sxs-lookup"><span data-stu-id="62768-107">Retrieves the Remote Desktop license server identifier if the server is currently activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="62768-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62768-108">Syntax</span></span>


```mof
uint32 GetLicenseServerId(
  [out] string sLicenseServerId
);
```



## <a name="parameters"></a><span data-ttu-id="62768-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62768-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62768-110">*sLicenseServerId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="62768-110">*sLicenseServerId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62768-111">Identificateur du serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="62768-111">Remote Desktop license server identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62768-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="62768-112">Return value</span></span>

<span data-ttu-id="62768-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="62768-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="62768-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="62768-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="62768-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="62768-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="62768-116">Notes</span><span class="sxs-lookup"><span data-stu-id="62768-116">Remarks</span></span>

<span data-ttu-id="62768-117">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="62768-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="62768-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="62768-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="62768-119">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="62768-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="62768-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="62768-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="62768-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="62768-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="62768-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62768-122">Requirements</span></span>



| <span data-ttu-id="62768-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62768-123">Requirement</span></span> | <span data-ttu-id="62768-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="62768-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="62768-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62768-125">Minimum supported client</span></span><br/> | <span data-ttu-id="62768-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="62768-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="62768-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62768-127">Minimum supported server</span></span><br/> | <span data-ttu-id="62768-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62768-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="62768-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="62768-129">Namespace</span></span><br/>                | <span data-ttu-id="62768-130">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="62768-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="62768-131">MOF</span><span class="sxs-lookup"><span data-stu-id="62768-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62768-132"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62768-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="62768-133">DLL</span><span class="sxs-lookup"><span data-stu-id="62768-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62768-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62768-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62768-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62768-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62768-136">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="62768-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

