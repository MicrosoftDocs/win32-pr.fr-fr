---
description: Récupère les informations du certificat.
ms.assetid: 57f1c6f9-f06d-4ac7-9070-2a2e6afe93d2
title: 'ICertificate2 :: GetInfo, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.GetInfo
- ICertificate2.GetInfo
- ICertificate.GetInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41b3cb6cde796f64ee3a5953ed848d105a10bc5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528432"
---
# <a name="icertificate2getinfo-method"></a><span data-ttu-id="6c5c3-103">ICertificate2 :: GetInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="6c5c3-103">ICertificate2::GetInfo method</span></span>

<span data-ttu-id="6c5c3-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="6c5c3-105">Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="6c5c3-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6c5c3-106">La méthode **GetInfo** récupère les informations du [*certificat*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="6c5c3-106">The **GetInfo** method retrieves information from the [*certificate*](../secgloss/c-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6c5c3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c5c3-107">Syntax</span></span>


```VB
Certificate.GetInfo( _
  ByVal InfoType _
)
```



## <a name="parameters"></a><span data-ttu-id="6c5c3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c5c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c5c3-109">*Infotype* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6c5c3-109">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c5c3-110">Valeur de l’énumération de [**\_ \_ \_ type informations du certificat CAPICOM**](capicom-cert-info-type.md) qui spécifie le type de données extraites du certificat.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-110">A value of the [**CAPICOM\_CERT\_INFO\_TYPE**](capicom-cert-info-type.md) enumeration that specifies what type of data is retrieved from the certificate.</span></span> <span data-ttu-id="6c5c3-111">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="6c5c3-112">Value</span><span class="sxs-lookup"><span data-stu-id="6c5c3-112">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="6c5c3-113">Signification</span><span class="sxs-lookup"><span data-stu-id="6c5c3-113">Meaning</span></span>                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERT_INFO_SUBJECT_SIMPLE_NAME"></span><span id="capicom_cert_info_subject_simple_name"></span><dl> <span data-ttu-id="6c5c3-114"><dt>**\_ \_ \_ \_ \_ nom simple de l’objet du certificat CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="6c5c3-114"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_SIMPLE\_NAME**</dt></span></span> </dl> | <span data-ttu-id="6c5c3-115">Retourne le nom complet de l’objet du certificat.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-115">Returns the display name from the certificate subject.</span></span><br/>                            |
| <span id="CAPICOM_CERT_INFO_ISSUER_SIMPLE_NAME"></span><span id="capicom_cert_info_issuer_simple_name"></span><dl> <span data-ttu-id="6c5c3-116"><dt>**\_ \_ \_ \_ \_ nom simple de l’émetteur d’informations de certificat CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="6c5c3-116"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_SIMPLE\_NAME**</dt></span></span> </dl>    | <span data-ttu-id="6c5c3-117">Retourne le nom complet de l’émetteur du certificat.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-117">Returns the display name of the issuer of the certificate.</span></span><br/>                        |
| <span id="CAPICOM_CERT_INFO_SUBJECT_EMAIL_NAME"></span><span id="capicom_cert_info_subject_email_name"></span><dl> <span data-ttu-id="6c5c3-118"><dt>**nom du message de l’objet de l' \_ information du certificat CAPICOM \_ \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c5c3-118"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_EMAIL\_NAME**</dt></span></span> </dl>    | <span data-ttu-id="6c5c3-119">Retourne l’adresse de messagerie de l’objet du certificat.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-119">Returns the email address of the certificate subject.</span></span><br/>                             |
| <span id="CAPICOM_CERT_INFO_ISSUER_EMAIL_NAME"></span><span id="capicom_cert_info_issuer_email_name"></span><dl> <span data-ttu-id="6c5c3-120"><dt>**nom de messagerie de l' \_ émetteur du certificat CAPICOM \_ info \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c5c3-120"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_EMAIL\_NAME**</dt></span></span> </dl>       | <span data-ttu-id="6c5c3-121">Retourne l’adresse de messagerie de l’émetteur du certificat.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-121">Returns the email address of the issuer of the certificate.</span></span><br/>                       |
| <span id="CAPICOM_CERT_INFO_SUBJECT_UPN"></span><span id="capicom_cert_info_subject_upn"></span><dl> <span data-ttu-id="6c5c3-122"><dt>**UPN de l' \_ \_ objet d’informations de certificat CAPICOM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c5c3-122"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_UPN**</dt></span></span> </dl>                          | <span data-ttu-id="6c5c3-123">Retourne l’UPN de l’objet du certificat.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-123">Returns the UPN of the certificate subject.</span></span> <span data-ttu-id="6c5c3-124">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-124">Introduced in CAPICOM 2.0.</span></span><br/>            |
| <span id="CAPICOM_CERT_INFO_ISSUER_UPN"></span><span id="capicom_cert_info_issuer_upn"></span><dl> <span data-ttu-id="6c5c3-125"><dt>**UPN de l' \_ \_ émetteur des informations de certificat CAPICOM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c5c3-125"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_UPN**</dt></span></span> </dl>                             | <span data-ttu-id="6c5c3-126">Retourne l’UPN de l’émetteur du certificat.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-126">Returns the UPN of the issuer of the certificate.</span></span> <span data-ttu-id="6c5c3-127">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-127">Introduced in CAPICOM 2.0.</span></span><br/>      |
| <span id="CAPICOM_CERT_INFO_SUBJECT_DNS_NAME"></span><span id="capicom_cert_info_subject_dns_name"></span><dl> <span data-ttu-id="6c5c3-128"><dt>**\_ \_ \_ \_ \_ nom DNS de l’objet du certificat CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="6c5c3-128"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_DNS\_NAME**</dt></span></span> </dl>          | <span data-ttu-id="6c5c3-129">Retourne le nom DNS de l’objet du certificat.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-129">Returns the DNS name of the certificate subject.</span></span> <span data-ttu-id="6c5c3-130">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-130">Introduced in CAPICOM 2.0.</span></span><br/>       |
| <span id="CAPICOM_CERT_INFO_ISSUER_DNS_NAME"></span><span id="capicom_cert_info_issuer_dns_name"></span><dl> <span data-ttu-id="6c5c3-131"><dt>**\_ \_ \_ \_ nom DNS de l’émetteur CAPICOM informations CERT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c5c3-131"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_DNS\_NAME**</dt></span></span> </dl>             | <span data-ttu-id="6c5c3-132">Retourne le nom DNS de l’émetteur du certificat.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-132">Returns the DNS name of the issuer of the certificate.</span></span> <span data-ttu-id="6c5c3-133">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-133">Introduced in CAPICOM 2.0.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c5c3-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6c5c3-134">Return value</span></span>

<span data-ttu-id="6c5c3-135">Chaîne qui contient les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-135">A string that contains the requested information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c5c3-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c5c3-136">Requirements</span></span>



| <span data-ttu-id="6c5c3-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c5c3-137">Requirement</span></span> | <span data-ttu-id="6c5c3-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c5c3-138">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c5c3-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="6c5c3-139">End of client support</span></span><br/> | <span data-ttu-id="6c5c3-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c5c3-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6c5c3-141">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="6c5c3-141">End of server support</span></span><br/> | <span data-ttu-id="6c5c3-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c5c3-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6c5c3-143">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="6c5c3-143">Redistributable</span></span><br/>       | <span data-ttu-id="6c5c3-144">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c5c3-144">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6c5c3-145">DLL</span><span class="sxs-lookup"><span data-stu-id="6c5c3-145">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6c5c3-146"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c5c3-146"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c5c3-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c5c3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c5c3-148">Objets de chiffrement</span><span class="sxs-lookup"><span data-stu-id="6c5c3-148">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="6c5c3-149">**Certificat**</span><span class="sxs-lookup"><span data-stu-id="6c5c3-149">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
