---
description: La méthode FileSignatureInfo de l’objet installer prend le chemin d’accès à un fichier et retourne un SAFEARRAY d’octets qui représentent le hachage ou le certificat encodé.
ms.assetid: ab34bc46-8a8f-4b48-a1d1-d824ff36a9cc
title: Installer. FileSignatureInfo, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSignatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5dbb758118b7612aaef3f7cca744674bca1c768d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520792"
---
# <a name="installerfilesignatureinfo-method"></a><span data-ttu-id="22861-103">Installer. FileSignatureInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="22861-103">Installer.FileSignatureInfo method</span></span>

<span data-ttu-id="22861-104">La méthode **FileSignatureInfo** de l’objet [**installer**](installer-object.md) prend le chemin d’accès à un fichier et retourne un SAFEARRAY d’octets qui représentent le hachage ou le certificat encodé.</span><span class="sxs-lookup"><span data-stu-id="22861-104">The **FileSignatureInfo** method of the [**Installer**](installer-object.md) object takes the path to a file and returns a SAFEARRAY of bytes that represent the hash or the encoded certificate.</span></span> <span data-ttu-id="22861-105">Les valeurs peuvent ensuite être utilisées pour remplir les tables [MsiDigitalSignature](msidigitalsignature-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)et [MsiDigitalCertificate](msidigitalcertificate-table.md) .</span><span class="sxs-lookup"><span data-stu-id="22861-105">The values can then be used to populate the [MsiDigitalSignature](msidigitalsignature-table.md), [MsiPatchCertificate](msipatchcertificate-table.md), and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables.</span></span>

<span data-ttu-id="22861-106">Pour plus d’informations, consultez [**type de données SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span><span class="sxs-lookup"><span data-stu-id="22861-106">For more information, see the [**SAFEARRAY Data Type**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span>

## <a name="syntax"></a><span data-ttu-id="22861-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22861-107">Syntax</span></span>


```JScript
Installer.FileSignatureInfo(
  FilePath,
  Options,
  Format
)
```



## <a name="parameters"></a><span data-ttu-id="22861-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22861-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22861-109">*FilePath*</span><span class="sxs-lookup"><span data-stu-id="22861-109">*FilePath*</span></span> 
</dt> <dd>

<span data-ttu-id="22861-110">Chemin d’accès complet à un fichier signé numériquement.</span><span class="sxs-lookup"><span data-stu-id="22861-110">Full path to a file that is digitally signed.</span></span>

<span data-ttu-id="22861-111">Lors du remplissage des tables [MsiDigitalSignature](msidigitalsignature-table.md) et [MsiDigitalCertificate](msidigitalcertificate-table.md) , *filePath* pointe vers une armoire signée numériquement.</span><span class="sxs-lookup"><span data-stu-id="22861-111">When populating the [MsiDigitalSignature](msidigitalsignature-table.md) and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables, *FilePath* points to a digitally signed cabinet.</span></span> <span data-ttu-id="22861-112">Lors du remplissage des tables [MsiPatchCertificate](msipatchcertificate-table.md) et MsiDigitalCertificate, *filePath* pointe vers un correctif signé numériquement.</span><span class="sxs-lookup"><span data-stu-id="22861-112">When populating the [MsiPatchCertificate](msipatchcertificate-table.md) and MsiDigitalCertificate tables, *FilePath* points to a digitally signed patch.</span></span>

</dd> <dt>

<span data-ttu-id="22861-113">*Options*</span><span class="sxs-lookup"><span data-stu-id="22861-113">*Options*</span></span> 
</dt> <dd>

<span data-ttu-id="22861-114">Indicateurs de cas d’erreur spéciaux.</span><span class="sxs-lookup"><span data-stu-id="22861-114">Special error case flags.</span></span>



| <span data-ttu-id="22861-115">Indicateur</span><span class="sxs-lookup"><span data-stu-id="22861-115">Flag</span></span>                                                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="22861-116">Signification</span><span class="sxs-lookup"><span data-stu-id="22861-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiSignatureOptionInvalidHashFatal"></span><span id="msisignatureoptioninvalidhashfatal"></span><span id="MSISIGNATUREOPTIONINVALIDHASHFATAL"></span><dl> <span data-ttu-id="22861-117"><dt>**msiSignatureOptionInvalidHashFatal**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="22861-117"><dt>**msiSignatureOptionInvalidHashFatal**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="22861-118">Avec les *options* définies sur MsiSignatureOptionInvalidHashFatal, **FileSignatureInfo** retourne toujours une erreur irrécupérable pour un hachage non valide.</span><span class="sxs-lookup"><span data-stu-id="22861-118">With *Options* set to msiSignatureOptionInvalidHashFatal, **FileSignatureInfo** always returns a fatal error for an invalid hash.</span></span> <br/> <span data-ttu-id="22861-119">Si *options* n’a pas la valeur msiSignatureOptionInvalidHashFatal et que *format* a la valeur msiSignatureInfoCertificate, **FileSignatureInfo** ne retourne pas d’erreur pour un hachage non valide.</span><span class="sxs-lookup"><span data-stu-id="22861-119">If *Options* is not set to msiSignatureOptionInvalidHashFatal and *Format* is set to msiSignatureInfoCertificate, **FileSignatureInfo** does not return an error for an invalid hash.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="22861-120">*Format*</span><span class="sxs-lookup"><span data-stu-id="22861-120">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="22861-121">Informations de signature demandées.</span><span class="sxs-lookup"><span data-stu-id="22861-121">The requested signature information.</span></span>



| <span data-ttu-id="22861-122">Indicateur</span><span class="sxs-lookup"><span data-stu-id="22861-122">Flag</span></span>                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="22861-123">Signification</span><span class="sxs-lookup"><span data-stu-id="22861-123">Meaning</span></span>                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="msiSignatureInfoCertificate"></span><span id="msisignatureinfocertificate"></span><span id="MSISIGNATUREINFOCERTIFICATE"></span><dl> <span data-ttu-id="22861-124"><dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="22861-124"><dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="22861-125">Retourne un SAFEARRAY d’octets qui représentent le certificat encodé.</span><span class="sxs-lookup"><span data-stu-id="22861-125">Returns a SAFEARRAY of bytes that represent the encoded certificate.</span></span><br/> |
| <span id="msiSignatureInfoHash"></span><span id="msisignatureinfohash"></span><span id="MSISIGNATUREINFOHASH"></span><dl> <span data-ttu-id="22861-126"><dt>**msiSignatureInfoHash**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="22861-126"><dt>**msiSignatureInfoHash**</dt> <dt>1</dt></span></span> </dl>                             | <span data-ttu-id="22861-127">Retourne un SAFEARRAY d’octets qui représentent le hachage.</span><span class="sxs-lookup"><span data-stu-id="22861-127">Returns a SAFEARRAY of bytes that represent the hash.</span></span><br/>                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22861-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22861-128">Return value</span></span>

<span data-ttu-id="22861-129">En cas de réussite, la méthode retourne un [SAFEARRAY](/windows/win32/api/oaidl/ns-oaidl-safearray) d’octets qui contiennent le hachage ou le certificat encodé.</span><span class="sxs-lookup"><span data-stu-id="22861-129">If successful, the method returns a [SAFEARRAY](/windows/win32/api/oaidl/ns-oaidl-safearray) of bytes that contain either the hash or encoded certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="22861-130">Notes</span><span class="sxs-lookup"><span data-stu-id="22861-130">Remarks</span></span>

<span data-ttu-id="22861-131">Pour créer une installation signée entièrement vérifiée à l’aide de l’automatisation, utilisez la méthode **FileSignatureInfo** pour remplir les tables [MsiDigitalCertificate](msidigitalcertificate-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)et [MsiDigitalSignature](msidigitalsignature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="22861-131">To author a fully verified signed installation by using automation, use the **FileSignatureInfo** method to populate the [MsiDigitalCertificate](msidigitalcertificate-table.md), [MsiPatchCertificate](msipatchcertificate-table.md), and [MsiDigitalSignature](msidigitalsignature-table.md) tables.</span></span> <span data-ttu-id="22861-132">Pour plus d’informations, consultez [création d’une installation signée entièrement vérifiée à l’aide d’Automation](authoring-a-fully-verified-signed-installation-using-automation.md).</span><span class="sxs-lookup"><span data-stu-id="22861-132">For more information, see [Authoring a Fully Verified Signed Installation Using Automation](authoring-a-fully-verified-signed-installation-using-automation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22861-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22861-133">Requirements</span></span>



| <span data-ttu-id="22861-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22861-134">Requirement</span></span> | <span data-ttu-id="22861-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="22861-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22861-136">Version</span><span class="sxs-lookup"><span data-stu-id="22861-136">Version</span></span><br/> | <span data-ttu-id="22861-137">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="22861-137">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="22861-138">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="22861-138">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="22861-139">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="22861-139">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="22861-140">DLL</span><span class="sxs-lookup"><span data-stu-id="22861-140">DLL</span></span><br/>     | <dl> <span data-ttu-id="22861-141"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22861-141"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="22861-142">IID</span><span class="sxs-lookup"><span data-stu-id="22861-142">IID</span></span><br/>     | <span data-ttu-id="22861-143">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="22861-143">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="22861-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22861-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22861-145">Création d’une installation signée entièrement vérifiée à l’aide d’Automation</span><span class="sxs-lookup"><span data-stu-id="22861-145">Authoring a Fully Verified Signed Installation Using Automation</span></span>](authoring-a-fully-verified-signed-installation-using-automation.md)
</dt> <dt>

[<span data-ttu-id="22861-146">Signatures numériques et Windows Installer</span><span class="sxs-lookup"><span data-stu-id="22861-146">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> <dt>

[<span data-ttu-id="22861-147">**MsiGetFileSignatureInformation**</span><span class="sxs-lookup"><span data-stu-id="22861-147">**MsiGetFileSignatureInformation**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> </dl>

 

 
