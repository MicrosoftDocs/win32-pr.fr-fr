---
description: Enregistre les objets de certificat dans la collection.
ms.assetid: 1d4b7bd5-3ed3-4ace-9894-4e89c5cf844f
title: Certificates. Save, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36ab04b394bddcd829d9f15e7562b72125388d33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526465"
---
# <a name="certificatessave-method"></a><span data-ttu-id="d9c16-103">Certificates. Save, méthode</span><span class="sxs-lookup"><span data-stu-id="d9c16-103">Certificates.Save method</span></span>

<span data-ttu-id="d9c16-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d9c16-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d9c16-105">Utilisez plutôt la [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="d9c16-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d9c16-106">La méthode **Save** enregistre les objets de [**certificat**](certificate.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="d9c16-106">The **Save** method saves the [**Certificate**](certificate.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9c16-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9c16-107">Syntax</span></span>


```VB
Certificates.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal ExportFlag ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d9c16-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9c16-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9c16-109">*Nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d9c16-109">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9c16-110">Chaîne qui contient le nom du fichier de sortie dans lequel les certificats seront enregistrés.</span><span class="sxs-lookup"><span data-stu-id="d9c16-110">A string that contains the name of the output file where the certificates will be saved.</span></span>

</dd> <dt>

<span data-ttu-id="d9c16-111">*Mot de passe* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d9c16-111">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d9c16-112">Chaîne qui contient le mot de passe en [*texte clair*](../secgloss/p-gly.md) pour un fichier de [*clé privée*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d9c16-112">A string that contains the [*plaintext*](../secgloss/p-gly.md) password for a [*private key*](../secgloss/p-gly.md) file.</span></span> <span data-ttu-id="d9c16-113">La valeur par défaut est la chaîne vide ("").</span><span class="sxs-lookup"><span data-stu-id="d9c16-113">The default value is the empty string ("").</span></span> <span data-ttu-id="d9c16-114">Jusqu’à 32 caractères Unicode, y compris un caractère null de fin, peuvent être utilisés pour le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="d9c16-114">Up to 32 Unicode characters, including a terminating null character, can be used for the password.</span></span> <span data-ttu-id="d9c16-115">Pour plus d’informations sur la protection du mot de passe, consultez [gestion des mots de passe](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="d9c16-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9c16-116">*Enregistreras* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d9c16-116">*SaveAs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d9c16-117">Valeur de l’énumération des [**\_ certificats CAPICOM \_ \_ sous forme de \_ type**](capicom-certificates-save-as-type.md) qui spécifie le format du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="d9c16-117">A value of the [**CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE**](capicom-certificates-save-as-type.md) enumeration that specifies the format of the output file.</span></span> <span data-ttu-id="d9c16-118">La valeur par défaut est CAPICOM \_ certificats \_ Enregistrer \_ comme \_ pfx.</span><span class="sxs-lookup"><span data-stu-id="d9c16-118">The default is CAPICOM\_CERTIFICATES\_SAVE\_AS\_PFX.</span></span> <span data-ttu-id="d9c16-119">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="d9c16-119">The following table shows the possible values.</span></span>



| <span data-ttu-id="d9c16-120">Value</span><span class="sxs-lookup"><span data-stu-id="d9c16-120">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="d9c16-121">Signification</span><span class="sxs-lookup"><span data-stu-id="d9c16-121">Meaning</span></span>                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PFX"></span><span id="capicom_certificates_save_as_pfx"></span><dl> <span data-ttu-id="d9c16-122"><dt>**\_certificats CAPICOM \_ Enregistrer \_ comme \_ pfx**</dt></span><span class="sxs-lookup"><span data-stu-id="d9c16-122"><dt>**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PFX**</dt></span></span> </dl>                      | <span data-ttu-id="d9c16-123">Les certificats sont enregistrés en tant que PFX.</span><span class="sxs-lookup"><span data-stu-id="d9c16-123">The certificates are saved as a PFX.</span></span><br/>      |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PKCS7"></span><span id="capicom_certificates_save_as_pkcs7"></span><dl> <span data-ttu-id="d9c16-124"><dt>**\_Certificats CAPICOM \_ enregistrés \_ en tant que \_ PKCS7**</dt></span><span class="sxs-lookup"><span data-stu-id="d9c16-124"><dt>**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PKCS7**</dt></span></span> </dl>                | <span data-ttu-id="d9c16-125">Les certificats sont enregistrés sous la forme d’un fichier PKCS \# 7.</span><span class="sxs-lookup"><span data-stu-id="d9c16-125">The certificates are saved as a PKCS \#7.</span></span><br/> |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_SERIALIZED"></span><span id="capicom_certificates_save_as_serialized"></span><dl> <span data-ttu-id="d9c16-126"><dt>**\_certificats CAPICOM \_ enregistrés \_ sous forme \_ sérialisée**</dt></span><span class="sxs-lookup"><span data-stu-id="d9c16-126"><dt>**CAPICOM\_CERTIFICATES\_SAVE\_AS\_SERIALIZED**</dt></span></span> </dl> | <span data-ttu-id="d9c16-127">Les certificats sont enregistrés sous forme sérialisée.</span><span class="sxs-lookup"><span data-stu-id="d9c16-127">The certificates are saved as serialized.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d9c16-128">*ExportFlag* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d9c16-128">*ExportFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d9c16-129">Valeur de l’énumération de l' [**\_ \_ indicateur d’exportation CAPICOM**](capicom-export-flag.md) qui spécifie si les erreurs d’exportation de clé privée sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="d9c16-129">A value of the [**CAPICOM\_EXPORT\_FLAG**](capicom-export-flag.md) enumeration that specifies whether any private key export errors are ignored.</span></span> <span data-ttu-id="d9c16-130">La valeur par défaut est la valeur par défaut d' \_ exportation CAPICOM \_ .</span><span class="sxs-lookup"><span data-stu-id="d9c16-130">The default is CAPICOM\_EXPORT\_DEFAULT.</span></span> <span data-ttu-id="d9c16-131">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="d9c16-131">The following table shows the possible values.</span></span>



| <span data-ttu-id="d9c16-132">Value</span><span class="sxs-lookup"><span data-stu-id="d9c16-132">Value</span></span>                                                                                                                                                                                                                                                                                          | <span data-ttu-id="d9c16-133">Signification</span><span class="sxs-lookup"><span data-stu-id="d9c16-133">Meaning</span></span>                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="CAPICOM_EXPORT_DEFAULT"></span><span id="capicom_export_default"></span><dl> <span data-ttu-id="d9c16-134"><dt>**\_ \_ valeur par défaut d’exportation CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="d9c16-134"><dt>**CAPICOM\_EXPORT\_DEFAULT**</dt></span></span> </dl>                                                                                                      | <span data-ttu-id="d9c16-135">Les erreurs d’exportation de clé privée ne sont pas ignorées.</span><span class="sxs-lookup"><span data-stu-id="d9c16-135">Private key export errors are not ignored.</span></span><br/> |
| <span id="CAPICOM_EXPORT_IGNORE_PRIVATE_KEY_NOT_EXPORTABLE_ERROR"></span><span id="capicom_export_ignore_private_key_not_exportable_error"></span><dl> <span data-ttu-id="d9c16-136"><dt>**\_erreur Impossible d’exporter \_ la \_ \_ clé privée \_ \_ d’exportation \_ CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="d9c16-136"><dt>**CAPICOM\_EXPORT\_IGNORE\_PRIVATE\_KEY\_NOT\_EXPORTABLE\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="d9c16-137">Les erreurs d’exportation de clé privée sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="d9c16-137">Private key export errors are ignored.</span></span><br/>     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9c16-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d9c16-138">Return value</span></span>

<span data-ttu-id="d9c16-139">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d9c16-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9c16-140">Notes</span><span class="sxs-lookup"><span data-stu-id="d9c16-140">Remarks</span></span>

<span data-ttu-id="d9c16-141">Cette méthode génère un CAPICOM \_ E \_ non \_ autorisé lorsqu’il est fait un script à partir d’une application Web.</span><span class="sxs-lookup"><span data-stu-id="d9c16-141">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

<span data-ttu-id="d9c16-142">Les objets de [**certificat**](certificate.md) peuvent être récupérés à l’aide de la méthode [**Store. Load**](store-load.md) .</span><span class="sxs-lookup"><span data-stu-id="d9c16-142">The [**Certificate**](certificate.md) objects can be retrieved by using the [**Store.Load**](store-load.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9c16-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9c16-143">Requirements</span></span>



| <span data-ttu-id="d9c16-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9c16-144">Requirement</span></span> | <span data-ttu-id="d9c16-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9c16-145">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9c16-146">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d9c16-146">End of client support</span></span><br/> | <span data-ttu-id="d9c16-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9c16-147">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d9c16-148">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="d9c16-148">End of server support</span></span><br/> | <span data-ttu-id="d9c16-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9c16-149">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d9c16-150">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="d9c16-150">Redistributable</span></span><br/>       | <span data-ttu-id="d9c16-151">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="d9c16-151">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d9c16-152">DLL</span><span class="sxs-lookup"><span data-stu-id="d9c16-152">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d9c16-153"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9c16-153"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9c16-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9c16-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9c16-155">**Certificates**</span><span class="sxs-lookup"><span data-stu-id="d9c16-155">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
