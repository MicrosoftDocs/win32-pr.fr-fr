---
title: Méthode GenerateReportEx de la classe Win32_TSLicenseReport
description: Génère un rapport d’utilisation de licence en cours pour les licences par utilisateur et par périphérique.
ms.assetid: c454e0c5-ca1c-41c7-86b2-1e52c414aeb5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GenerateReportEx
- Services Bureau à distance de la méthode GenerateReportEx, classe Win32_TSLicenseReport
- Win32_TSLicenseReport de la classe Services Bureau à distance, méthode GenerateReportEx
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReportEx
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893e6e29d1e4716560b0f0f6b41e6109c89e2f5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384056"
---
# <a name="generatereportex-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="47c0e-106">Méthode GenerateReportEx de la \_ classe Win32 TSLicenseReport</span><span class="sxs-lookup"><span data-stu-id="47c0e-106">GenerateReportEx method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="47c0e-107">Génère un rapport d’utilisation de licence en cours pour les licences par utilisateur et par périphérique.</span><span class="sxs-lookup"><span data-stu-id="47c0e-107">Generates a current license usage report for both Per User and Per Device licenses.</span></span>

## <a name="syntax"></a><span data-ttu-id="47c0e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47c0e-108">Syntax</span></span>


```mof
uint32 GenerateReportEx(
  [out] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="47c0e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47c0e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47c0e-110">*Nom du fichier* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="47c0e-110">*FileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47c0e-111">Nom de fichier du rapport généré.</span><span class="sxs-lookup"><span data-stu-id="47c0e-111">The file name of the generated report.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47c0e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="47c0e-112">Return value</span></span>

<span data-ttu-id="47c0e-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="47c0e-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="47c0e-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="47c0e-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="47c0e-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="47c0e-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="47c0e-116">Notes</span><span class="sxs-lookup"><span data-stu-id="47c0e-116">Remarks</span></span>

<span data-ttu-id="47c0e-117">Il s’agit d’une méthode statique.</span><span class="sxs-lookup"><span data-stu-id="47c0e-117">This is a static method.</span></span>

<span data-ttu-id="47c0e-118">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="47c0e-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="47c0e-119">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="47c0e-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="47c0e-120">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="47c0e-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="47c0e-121">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="47c0e-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="47c0e-122">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="47c0e-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="47c0e-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47c0e-123">Requirements</span></span>



| <span data-ttu-id="47c0e-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47c0e-124">Requirement</span></span> | <span data-ttu-id="47c0e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="47c0e-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="47c0e-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47c0e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="47c0e-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="47c0e-127">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="47c0e-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47c0e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="47c0e-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="47c0e-129">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="47c0e-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="47c0e-130">Namespace</span></span><br/>                | <span data-ttu-id="47c0e-131">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="47c0e-131">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="47c0e-132">MOF</span><span class="sxs-lookup"><span data-stu-id="47c0e-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47c0e-133"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47c0e-133"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="47c0e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="47c0e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47c0e-135"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47c0e-135"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47c0e-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47c0e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47c0e-137">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="47c0e-137">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

