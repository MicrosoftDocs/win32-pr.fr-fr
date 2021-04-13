---
description: Le dossier enrollCommon contient les fonctions d’assistance et les macros suivantes utilisées par les exemples fournis avec le kit de développement logiciel (SDK) d’inscription de certificats.
ms.assetid: a9b3532d-9640-4373-a6c6-7828cb6f55c7
title: enrollCommon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384a1f3741fd8bd7762c60da524e2e639c442e41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526998"
---
# <a name="enrollcommon"></a><span data-ttu-id="62638-103">enrollCommon</span><span class="sxs-lookup"><span data-stu-id="62638-103">enrollCommon</span></span>

<span data-ttu-id="62638-104">Le dossier enrollCommon contient les fonctions d’assistance et les macros suivantes utilisées par les exemples fournis avec le kit de développement logiciel (SDK) d’inscription de certificats.</span><span class="sxs-lookup"><span data-stu-id="62638-104">The enrollCommon folder contains the following helper functions and macros used by the samples provided with the Certificate Enrollment SDK.</span></span> <span data-ttu-id="62638-105">Il est installé par défaut dans le dossier *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ x509 Certificate \\ enrollCommon VC \\ .</span><span class="sxs-lookup"><span data-stu-id="62638-105">It is installed by default in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollCommon folder.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="62638-106">Fonction</span><span class="sxs-lookup"><span data-stu-id="62638-106">Function</span></span></th>
<th><span data-ttu-id="62638-107">Description</span><span class="sxs-lookup"><span data-stu-id="62638-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="62638-108">_JumpIfError</span><span class="sxs-lookup"><span data-stu-id="62638-108">_JumpIfError</span></span></td>
<td><span data-ttu-id="62638-109">Macro qui accepte une valeur <strong>HRESULT</strong> , une étiquette et une chaîne d’erreur, imprime la chaîne et transfère le contrôle du programme à la première instruction qui suit l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="62638-109">Macro that accepts an <strong>HRESULT</strong> value, a label, and an error string, prints the string, and transfers program control to the first statement following the label.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62638-110">_JumpError</span><span class="sxs-lookup"><span data-stu-id="62638-110">_JumpError</span></span></td>
<td><span data-ttu-id="62638-111">Identique à la macro _JumpIfError.</span><span class="sxs-lookup"><span data-stu-id="62638-111">Same as the _JumpIfError macro.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62638-112">_PrintIfError</span><span class="sxs-lookup"><span data-stu-id="62638-112">_PrintIfError</span></span></td>
<td><span data-ttu-id="62638-113">Pas utilisé pour l'instant.</span><span class="sxs-lookup"><span data-stu-id="62638-113">Not currently used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62638-114">_PrintError</span><span class="sxs-lookup"><span data-stu-id="62638-114">_PrintError</span></span></td>
<td><span data-ttu-id="62638-115">Macro qui imprime un message d’erreur et une valeur <strong>HRESULT</strong> .</span><span class="sxs-lookup"><span data-stu-id="62638-115">Macro that prints an error message and an <strong>HRESULT</strong> value.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62638-116">convertWszToSz</span><span class="sxs-lookup"><span data-stu-id="62638-116">convertWszToSz</span></span></td>
<td><span data-ttu-id="62638-117">Convertit une chaîne de caractères larges en une chaîne de caractères ASCII à l’aide de la fonction <strong>WideCharToMultiByte</strong> et de l’identificateur de page de codes ANSI actuel du système.</span><span class="sxs-lookup"><span data-stu-id="62638-117">Converts a wide-character string to an ASCII character string by using the <strong>WideCharToMultiByte</strong> function and the current ANSI code-page identifier for the system.</span></span> <span data-ttu-id="62638-118">Cette fonction est utilisée par les fonctions decConvertFromUnicode et findOIDFromTemplateName définies dans enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="62638-118">This function is used by the decConvertFromUnicode and findOIDFromTemplateName functions defined in enrollCommon.cpp.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62638-119">convertSzToWsz</span><span class="sxs-lookup"><span data-stu-id="62638-119">convertSzToWsz</span></span></td>
<td><span data-ttu-id="62638-120">Convertit une chaîne ASCII en une chaîne de caractères larges à l’aide de la fonction <strong>MultiByteToWideChar</strong> et de l’identificateur de page de codes ANSI actuel du système.</span><span class="sxs-lookup"><span data-stu-id="62638-120">Converts an ASCII string to a wide-character string by using the <strong>MultiByteToWideChar</strong> function and the current ANSI code-page identifier for the system.</span></span> <span data-ttu-id="62638-121">Cette fonction est utilisée par la fonction findCertByTemplate définie dans enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="62638-121">This function is used by the findCertByTemplate function defined in enrollCommon.cpp.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62638-122">convertSzToBstr</span><span class="sxs-lookup"><span data-stu-id="62638-122">convertSzToBstr</span></span></td>
<td><span data-ttu-id="62638-123">Convertit une chaîne ASCII en <strong>BSTR</strong> à l’aide de la fonction <strong>MultiByteToWideChar</strong> .</span><span class="sxs-lookup"><span data-stu-id="62638-123">Converts an ASCII string to a <strong>BSTR</strong> by using the <strong>MultiByteToWideChar</strong> function.</span></span> <span data-ttu-id="62638-124">Cette fonction n’est pas utilisée actuellement.</span><span class="sxs-lookup"><span data-stu-id="62638-124">This function is not currently used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62638-125">convertWszToBstr</span><span class="sxs-lookup"><span data-stu-id="62638-125">convertWszToBstr</span></span></td>
<td><span data-ttu-id="62638-126">Convertit une chaîne de caractères larges en <strong>BSTR</strong>.</span><span class="sxs-lookup"><span data-stu-id="62638-126">Converts a wide-character string to a <strong>BSTR</strong>.</span></span> <span data-ttu-id="62638-127">Cette fonction est utilisée par l’exemple installResponseFromPFX.</span><span class="sxs-lookup"><span data-stu-id="62638-127">This function is used by the installResponseFromPFX sample.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62638-128">checkEnrollStatus</span><span class="sxs-lookup"><span data-stu-id="62638-128">checkEnrollStatus</span></span></td>
<td><span data-ttu-id="62638-129">Vérifie l’état du processus d’inscription de certificats à l’aide des interfaces <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> et <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="62638-129">Checks the status of the certificate enrollment process by using the <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> and <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus</strong></a> interfaces.</span></span> <span data-ttu-id="62638-130">Cette fonction est utilisée par les exemples enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert et enrollSimpleUserCert.</span><span class="sxs-lookup"><span data-stu-id="62638-130">This function is used by the enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert, and enrollSimpleUserCert samples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62638-131">findCertByKeyUsage</span><span class="sxs-lookup"><span data-stu-id="62638-131">findCertByKeyUsage</span></span></td>
<td><span data-ttu-id="62638-132">Énumère le magasin de certificats personnels de l’utilisateur actuel pour rechercher le premier certificat pour lequel l’utilisation prévue de la clé publique correspond à une valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="62638-132">Enumerates the personal certificate store of the current user to find the first certificate for which the intended use of the public key matches a specified value.</span></span> <span data-ttu-id="62638-133">La valeur spécifiée peut être une combinaison au niveau du bit des indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="62638-133">The value specified can be a bitwise combination of the following flags:</span></span>
<ul>
<li><span data-ttu-id="62638-134">CERT_DATA_ENCIPHERMENT_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="62638-134">CERT_DATA_ENCIPHERMENT_KEY_USAGE</span></span></li>
<li><span data-ttu-id="62638-135">CERT_DIGITAL_SIGNATURE_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="62638-135">CERT_DIGITAL_SIGNATURE_KEY_USAGE</span></span></li>
<li><span data-ttu-id="62638-136">CERT_KEY_AGREEMENT_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="62638-136">CERT_KEY_AGREEMENT_KEY_USAGE</span></span></li>
<li><span data-ttu-id="62638-137">CERT_KEY_CERT_SIGN_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="62638-137">CERT_KEY_CERT_SIGN_KEY_USAGE</span></span></li>
<li><span data-ttu-id="62638-138">CERT_KEY_ENCIPHERMENT_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="62638-138">CERT_KEY_ENCIPHERMENT_KEY_USAGE</span></span></li>
<li><span data-ttu-id="62638-139">CERT_NON_REPUDIATION_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="62638-139">CERT_NON_REPUDIATION_KEY_USAGE</span></span></li>
<li><span data-ttu-id="62638-140">CERT_OFFLINE_CRL_SIGN_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="62638-140">CERT_OFFLINE_CRL_SIGN_KEY_USAGE</span></span></li>
</ul>
<span data-ttu-id="62638-141">Cette fonction est utilisée par l’exemple enrollFromPublicKey.</span><span class="sxs-lookup"><span data-stu-id="62638-141">This function is used by the enrollFromPublicKey sample.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62638-142">findCertByEKU</span><span class="sxs-lookup"><span data-stu-id="62638-142">findCertByEKU</span></span></td>
<td><span data-ttu-id="62638-143">Énumère le magasin de certificats personnels de l’utilisateur actuel pour rechercher le premier certificat pour lequel l’extension d’utilisation améliorée de la clé correspond à celle spécifiée en entrée.</span><span class="sxs-lookup"><span data-stu-id="62638-143">Enumerates the personal certificate store of the current user to find the first certificate for which the Enhanced Key Usage (EKU) extension matches that specified on input.</span></span> <span data-ttu-id="62638-144">Pour plus d’informations sur l’extension d’utilisation améliorée de la carte, consultez l’interface <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="62638-144">For more information about the EKU extension, see the <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage</strong></a> interface.</span></span> <span data-ttu-id="62638-145">Cette fonction est utilisée par l’exemple enrollEOBOCMC.</span><span class="sxs-lookup"><span data-stu-id="62638-145">This function is used by the enrollEOBOCMC sample.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62638-146">findCertByTemplate</span><span class="sxs-lookup"><span data-stu-id="62638-146">findCertByTemplate</span></span></td>
<td><span data-ttu-id="62638-147">Énumère le magasin de certificats personnels de l’utilisateur actuel pour rechercher le premier certificat pour lequel le modèle correspond à celui spécifié, par nom, en entrée.</span><span class="sxs-lookup"><span data-stu-id="62638-147">Enumerates the personal certificate store of the current user to find the first certificate for which the template matches that specified, by name, on input.</span></span> <span data-ttu-id="62638-148">Cette fonction est utilisée par les exemples enrollPKCS7 et enrollRenewalPKCS7.</span><span class="sxs-lookup"><span data-stu-id="62638-148">This function is used by the enrollPKCS7 and enrollRenewalPKCS7 samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62638-149">enrollCertByTemplate</span><span class="sxs-lookup"><span data-stu-id="62638-149">enrollCertByTemplate</span></span></td>
<td><span data-ttu-id="62638-150">Initialise un objet <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> à l’aide d’un modèle, tente d’inscrire la demande de certificat créée implicitement et surveille l’état du processus d’inscription.</span><span class="sxs-lookup"><span data-stu-id="62638-150">Initializes an <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> object by using a template, attempts to enroll the implicitly created certificate request, and monitors the status of the enrollment process.</span></span> <span data-ttu-id="62638-151">Cette fonction est utilisée par les exemples enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 et enrollRenewalPKCS7.</span><span class="sxs-lookup"><span data-stu-id="62638-151">This function is used by the enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7, and enrollRenewalPKCS7 samples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62638-152">verifyCertContext</span><span class="sxs-lookup"><span data-stu-id="62638-152">verifyCertContext</span></span></td>
<td><span data-ttu-id="62638-153">Vérifie la conformité de la chaîne de certificats par rapport à la stratégie (de base) spécifiée et, éventuellement, à l’extension d’utilisation améliorée de la clé spécifiée.</span><span class="sxs-lookup"><span data-stu-id="62638-153">Verifies compliance of the certificate chain against the specified (base) policy and, optionally, against a specified Enhanced Key Usage (EKU) extension.</span></span> <span data-ttu-id="62638-154">Pour plus d’informations, consultez la fonction <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>CertVerifyCertificateChainPolicy</strong></a> et les structures <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> et <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="62638-154">For more information, see the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>CertVerifyCertificateChainPolicy</strong></a> function and the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> and <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> structures.</span></span> <span data-ttu-id="62638-155">Cette fonction est utilisée par les exemples enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 et enrollRenewalPKCS7.</span><span class="sxs-lookup"><span data-stu-id="62638-155">This function is used by the enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7, and enrollRenewalPKCS7 samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62638-156">decConvertFromUnicode</span><span class="sxs-lookup"><span data-stu-id="62638-156">decConvertFromUnicode</span></span></td>
<td><span data-ttu-id="62638-157">Convertit une chaîne de caractères Unicode codés sur deux octets en une chaîne de caractères ANSI sur un octet.</span><span class="sxs-lookup"><span data-stu-id="62638-157">Converts a string of double-byte Unicode characters to a string of single-byte ANSI characters.</span></span> <span data-ttu-id="62638-158">Cette fonction est utilisée par la fonction DecodeFileW définie dans enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="62638-158">This function is used by the DecodeFileW function defined in enrollCommon.cpp.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62638-159">DecodeFileW</span><span class="sxs-lookup"><span data-stu-id="62638-159">DecodeFileW</span></span></td>
<td><span data-ttu-id="62638-160">Décode un certificat encodé ou un fichier de demande de certificat en un tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="62638-160">Decodes an encoded certificate or certificate request file to a byte array.</span></span> <span data-ttu-id="62638-161">Cette fonction est utilisée par l’exemple installResponseFromPFX.</span><span class="sxs-lookup"><span data-stu-id="62638-161">This function is used by the installResponseFromPFX sample.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62638-162">EncodeToFileW</span><span class="sxs-lookup"><span data-stu-id="62638-162">EncodeToFileW</span></span></td>
<td><span data-ttu-id="62638-163">Encode un certificat ou une demande de certificat et l’enregistre dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="62638-163">Encodes a certificate or certificate request and saves it to a file.</span></span> <span data-ttu-id="62638-164">Cette fonction est utilisée par les exemples createCNGCustomCMC, enrollEOBOCMC et enrollFromPublicKey.</span><span class="sxs-lookup"><span data-stu-id="62638-164">This function is used by the createCNGCustomCMC, enrollEOBOCMC, and enrollFromPublicKey samples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62638-165">findOIDFromTemplateName</span><span class="sxs-lookup"><span data-stu-id="62638-165">findOIDFromTemplateName</span></span></td>
<td><span data-ttu-id="62638-166">Récupère l’identificateur d’objet pour un modèle spécifié par nom.</span><span class="sxs-lookup"><span data-stu-id="62638-166">Retrieves the object identifier for a template specified by name.</span></span> <span data-ttu-id="62638-167">Cette fonction est utilisée par la fonction findCertByTemplate définie dans enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="62638-167">This function is used by the findCertByTemplate function defined in enrollCommon.cpp.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="62638-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="62638-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62638-169">Utilisation des exemples inclus</span><span class="sxs-lookup"><span data-stu-id="62638-169">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

