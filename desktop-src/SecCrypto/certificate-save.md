---
description: Enregistre le certificat dans un fichier.
ms.assetid: 2012b39b-47fd-4071-9752-98bb10954fc0
title: 'ICertificate2 :: Save, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Save
- ICertificate2.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3427feb86c705f5558d083bc39673fdf77553f58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530302"
---
# <a name="icertificate2save-method"></a><span data-ttu-id="cc031-103">ICertificate2 :: Save, méthode</span><span class="sxs-lookup"><span data-stu-id="cc031-103">ICertificate2::Save method</span></span>

<span data-ttu-id="cc031-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cc031-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="cc031-105">Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="cc031-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="cc031-106">La méthode **Save** enregistre le certificat dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="cc031-106">The **Save** method saves the certificate to a file.</span></span> <span data-ttu-id="cc031-107">Cette méthode a été introduite dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="cc031-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc031-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc031-108">Syntax</span></span>


```VB
Certificate.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal IncludeOption ] _
)
```



## <a name="parameters"></a><span data-ttu-id="cc031-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc031-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc031-110">*Nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc031-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc031-111">Chaîne qui contient le nom du fichier de sortie où le certificat sera enregistré.</span><span class="sxs-lookup"><span data-stu-id="cc031-111">A string that contains the name of the output file where the certificate will be saved.</span></span>

</dd> <dt>

<span data-ttu-id="cc031-112">*Mot de passe* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="cc031-112">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc031-113">Chaîne qui contient le mot de passe en [*texte clair*](../secgloss/p-gly.md) pour un fichier de [*clé privée*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="cc031-113">A string that contains the [*plaintext*](../secgloss/p-gly.md) password for a [*private key*](../secgloss/p-gly.md) file.</span></span> <span data-ttu-id="cc031-114">Le mot de passe peut contenir jusqu’à 32 caractères Unicode, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="cc031-114">The password can contain up to 32 Unicode characters, including a terminating null character.</span></span> <span data-ttu-id="cc031-115">Pour plus d’informations sur la protection du mot de passe, consultez [gestion des mots de passe](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="cc031-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc031-116">*Enregistreras* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="cc031-116">*SaveAs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc031-117">Valeur de l’énumération du [**\_ certificat CAPICOM \_ \_ sous forme de \_ type**](capicom-certificate-save-as-type.md) qui spécifie le format du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="cc031-117">A value of the [**CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE**](capicom-certificate-save-as-type.md) enumeration that specifies the format of the output file.</span></span> <span data-ttu-id="cc031-118">La valeur par défaut est le **\_ certificat CAPICOM \_ enregistré \_ comme \_ CER**.</span><span class="sxs-lookup"><span data-stu-id="cc031-118">The default is **CAPICOM\_CERTIFICATE\_SAVE\_AS\_CER**.</span></span> <span data-ttu-id="cc031-119">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="cc031-119">The following table shows the possible values.</span></span>



| <span data-ttu-id="cc031-120">Value</span><span class="sxs-lookup"><span data-stu-id="cc031-120">Value</span></span>                                                                                                                                                                                                                  | <span data-ttu-id="cc031-121">Signification</span><span class="sxs-lookup"><span data-stu-id="cc031-121">Meaning</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_CER"></span><span id="capicom_certificate_save_as_cer"></span><dl> <span data-ttu-id="cc031-122"><dt>**\_certificat CAPICOM \_ enregistré \_ comme \_ CER**</dt></span><span class="sxs-lookup"><span data-stu-id="cc031-122"><dt>**CAPICOM\_CERTIFICATE\_SAVE\_AS\_CER**</dt></span></span> </dl> | <span data-ttu-id="cc031-123">Le fichier de sortie sera au format de fichier. cer sans aucune clé privée enregistrée.</span><span class="sxs-lookup"><span data-stu-id="cc031-123">The output file will be formatted as a .cer file with no private keys saved.</span></span><br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_PFX"></span><span id="capicom_certificate_save_as_pfx"></span><dl> <span data-ttu-id="cc031-124"><dt>**\_certificat CAPICOM \_ enregistré \_ en tant que \_ pfx**</dt></span><span class="sxs-lookup"><span data-stu-id="cc031-124"><dt>**CAPICOM\_CERTIFICATE\_SAVE\_AS\_PFX**</dt></span></span> </dl> | <span data-ttu-id="cc031-125">Le fichier de sortie sera formaté en tant que fichier. pfx (PKCS \# 12) et toutes les clés privées associées qui peuvent être exportées seront également enregistrées.</span><span class="sxs-lookup"><span data-stu-id="cc031-125">The output file will be formatted as a .pfx (PKCS \#12) file and any associated private keys that are exportable will also be saved.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cc031-126">*IncludeOption* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="cc031-126">*IncludeOption* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc031-127">La valeur du [**\_ certificat CAPICOM \_ inclut \_**](capicom-certificate-include-option.md) l’énumération d’option qui spécifie le nombre de certificats de la chaîne qui sont enregistrés dans le fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="cc031-127">A value of the [**CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION**](capicom-certificate-include-option.md) enumeration that specifies how many certificates in the chain are saved to the output file.</span></span> <span data-ttu-id="cc031-128">La valeur par défaut est le \_ certificat CAPICOM \_ inclut \_ uniquement l' \_ entité End \_ .</span><span class="sxs-lookup"><span data-stu-id="cc031-128">The default is CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY.</span></span> <span data-ttu-id="cc031-129">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="cc031-129">The following table shows the possible values.</span></span>



| <span data-ttu-id="cc031-130">Value</span><span class="sxs-lookup"><span data-stu-id="cc031-130">Value</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="cc031-131">Signification</span><span class="sxs-lookup"><span data-stu-id="cc031-131">Meaning</span></span>                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <span data-ttu-id="cc031-132"><dt>**le certificat CAPICOM \_ \_ inclut une \_ chaîne \_ à l’exception \_ de la racine**</dt></span><span class="sxs-lookup"><span data-stu-id="cc031-132"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT**</dt></span></span> </dl> | <span data-ttu-id="cc031-133">Enregistre tous les certificats de la chaîne à l’exception de l’entité racine</span><span class="sxs-lookup"><span data-stu-id="cc031-133">Saves all certificates in the chain with the exception of the root entity</span></span><br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <span data-ttu-id="cc031-134"><dt>**le certificat CAPICOM \_ \_ inclut une \_ \_ chaîne entière**</dt></span><span class="sxs-lookup"><span data-stu-id="cc031-134"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_WHOLE\_CHAIN**</dt></span></span> </dl>                    | <span data-ttu-id="cc031-135">Enregistre la chaîne de certificats complète</span><span class="sxs-lookup"><span data-stu-id="cc031-135">Saves the complete certificate chain</span></span><br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <span data-ttu-id="cc031-136"><dt>**le certificat CAPICOM \_ \_ inclut \_ uniquement l' \_ entité \_ end**</dt></span><span class="sxs-lookup"><span data-stu-id="cc031-136"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY**</dt></span></span> </dl>       | <span data-ttu-id="cc031-137">Enregistre uniquement le certificat d’entité finale</span><span class="sxs-lookup"><span data-stu-id="cc031-137">Saves only the end entity certificate</span></span><br/>                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc031-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cc031-138">Return value</span></span>

<span data-ttu-id="cc031-139">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="cc031-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc031-140">Notes</span><span class="sxs-lookup"><span data-stu-id="cc031-140">Remarks</span></span>

<span data-ttu-id="cc031-141">Cette méthode génère un CAPICOM \_ E \_ non \_ autorisé lorsqu’il est fait un script à partir d’une application Web.</span><span class="sxs-lookup"><span data-stu-id="cc031-141">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc031-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc031-142">Requirements</span></span>



| <span data-ttu-id="cc031-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc031-143">Requirement</span></span> | <span data-ttu-id="cc031-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc031-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc031-145">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="cc031-145">End of client support</span></span><br/> | <span data-ttu-id="cc031-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cc031-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="cc031-147">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="cc031-147">End of server support</span></span><br/> | <span data-ttu-id="cc031-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc031-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="cc031-149">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="cc031-149">Redistributable</span></span><br/>       | <span data-ttu-id="cc031-150">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="cc031-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cc031-151">DLL</span><span class="sxs-lookup"><span data-stu-id="cc031-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="cc031-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc031-152"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
