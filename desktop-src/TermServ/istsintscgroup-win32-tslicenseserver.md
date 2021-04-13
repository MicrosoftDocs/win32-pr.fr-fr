---
title: Méthode IsTSinTSCGroup de la classe Win32_TSLicenseServer
description: Récupère une valeur indiquant si un serveur hôte de session Bureau à distance (hôte de session Bureau à distance) est membre du groupe local ordinateurs Terminal Server sur le serveur de licences Bureau à distance.
ms.assetid: 61c39928-3a2b-4a36-ae4e-b9597a12d5e7
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode IsTSinTSCGroup
- Services Bureau à distance de la méthode IsTSinTSCGroup, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode IsTSinTSCGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsTSinTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d666457f053c8fd48abd904d099bfbfa93a0de6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509277"
---
# <a name="istsintscgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="b3659-106">Méthode IsTSinTSCGroup de la \_ classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="b3659-106">IsTSinTSCGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="b3659-107">Récupère une valeur indiquant si un serveur hôte de session Bureau à distance (hôte de session Bureau à distance) est membre du groupe local ordinateurs Terminal Server sur le serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b3659-107">Retrieves whether a Remote Desktop Session Host (RD Session Host) server is a member of the Terminal Server Computers local group on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3659-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3659-108">Syntax</span></span>


```mof
uint32 IsTSinTSCGroup(
  [in]  string  tsname,
  [out] boolean IsMember
);
```



## <a name="parameters"></a><span data-ttu-id="b3659-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3659-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3659-110">*tsname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3659-110">*tsname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3659-111">Nom du serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b3659-111">Name of the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="b3659-112">*IsMember* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b3659-112">*IsMember* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3659-113">Valeur booléenne qui indique si le serveur hôte de session Bureau à distance est membre du groupe local ordinateurs Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="b3659-113">Boolean value that indicates whether the RD Session Host server is a member of the Terminal Server Computers local group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3659-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3659-114">Return value</span></span>

<span data-ttu-id="b3659-115">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="b3659-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b3659-116">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="b3659-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b3659-117">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b3659-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b3659-118">Notes</span><span class="sxs-lookup"><span data-stu-id="b3659-118">Remarks</span></span>

<span data-ttu-id="b3659-119">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b3659-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b3659-120">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="b3659-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b3659-121">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b3659-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b3659-122">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="b3659-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b3659-123">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b3659-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3659-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3659-124">Requirements</span></span>



| <span data-ttu-id="b3659-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3659-125">Requirement</span></span> | <span data-ttu-id="b3659-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3659-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3659-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3659-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b3659-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3659-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="b3659-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3659-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b3659-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3659-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="b3659-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b3659-131">Namespace</span></span><br/>                | <span data-ttu-id="b3659-132">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="b3659-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="b3659-133">MOF</span><span class="sxs-lookup"><span data-stu-id="b3659-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3659-134"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3659-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3659-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b3659-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3659-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3659-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3659-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3659-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3659-138">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="b3659-138">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

