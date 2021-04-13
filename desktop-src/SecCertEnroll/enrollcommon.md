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
# <a name="enrollcommon"></a>enrollCommon

Le dossier enrollCommon contient les fonctions d’assistance et les macros suivantes utilisées par les exemples fournis avec le kit de développement logiciel (SDK) d’inscription de certificats. Il est installé par défaut dans le dossier *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ x509 Certificate \\ enrollCommon VC \\ .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Fonction</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>_JumpIfError</td>
<td>Macro qui accepte une valeur <strong>HRESULT</strong> , une étiquette et une chaîne d’erreur, imprime la chaîne et transfère le contrôle du programme à la première instruction qui suit l’étiquette.</td>
</tr>
<tr class="even">
<td>_JumpError</td>
<td>Identique à la macro _JumpIfError.</td>
</tr>
<tr class="odd">
<td>_PrintIfError</td>
<td>Pas utilisé pour l'instant.</td>
</tr>
<tr class="even">
<td>_PrintError</td>
<td>Macro qui imprime un message d’erreur et une valeur <strong>HRESULT</strong> .</td>
</tr>
<tr class="odd">
<td>convertWszToSz</td>
<td>Convertit une chaîne de caractères larges en une chaîne de caractères ASCII à l’aide de la fonction <strong>WideCharToMultiByte</strong> et de l’identificateur de page de codes ANSI actuel du système. Cette fonction est utilisée par les fonctions decConvertFromUnicode et findOIDFromTemplateName définies dans enrollCommon. cpp.</td>
</tr>
<tr class="even">
<td>convertSzToWsz</td>
<td>Convertit une chaîne ASCII en une chaîne de caractères larges à l’aide de la fonction <strong>MultiByteToWideChar</strong> et de l’identificateur de page de codes ANSI actuel du système. Cette fonction est utilisée par la fonction findCertByTemplate définie dans enrollCommon. cpp.</td>
</tr>
<tr class="odd">
<td>convertSzToBstr</td>
<td>Convertit une chaîne ASCII en <strong>BSTR</strong> à l’aide de la fonction <strong>MultiByteToWideChar</strong> . Cette fonction n’est pas utilisée actuellement.</td>
</tr>
<tr class="even">
<td>convertWszToBstr</td>
<td>Convertit une chaîne de caractères larges en <strong>BSTR</strong>. Cette fonction est utilisée par l’exemple installResponseFromPFX.</td>
</tr>
<tr class="odd">
<td>checkEnrollStatus</td>
<td>Vérifie l’état du processus d’inscription de certificats à l’aide des interfaces <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> et <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus</strong></a> . Cette fonction est utilisée par les exemples enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert et enrollSimpleUserCert.</td>
</tr>
<tr class="even">
<td>findCertByKeyUsage</td>
<td>Énumère le magasin de certificats personnels de l’utilisateur actuel pour rechercher le premier certificat pour lequel l’utilisation prévue de la clé publique correspond à une valeur spécifiée. La valeur spécifiée peut être une combinaison au niveau du bit des indicateurs suivants :
<ul>
<li>CERT_DATA_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_DIGITAL_SIGNATURE_KEY_USAGE</li>
<li>CERT_KEY_AGREEMENT_KEY_USAGE</li>
<li>CERT_KEY_CERT_SIGN_KEY_USAGE</li>
<li>CERT_KEY_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_NON_REPUDIATION_KEY_USAGE</li>
<li>CERT_OFFLINE_CRL_SIGN_KEY_USAGE</li>
</ul>
Cette fonction est utilisée par l’exemple enrollFromPublicKey.<br/></td>
</tr>
<tr class="odd">
<td>findCertByEKU</td>
<td>Énumère le magasin de certificats personnels de l’utilisateur actuel pour rechercher le premier certificat pour lequel l’extension d’utilisation améliorée de la clé correspond à celle spécifiée en entrée. Pour plus d’informations sur l’extension d’utilisation améliorée de la carte, consultez l’interface <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage</strong></a> . Cette fonction est utilisée par l’exemple enrollEOBOCMC.</td>
</tr>
<tr class="even">
<td>findCertByTemplate</td>
<td>Énumère le magasin de certificats personnels de l’utilisateur actuel pour rechercher le premier certificat pour lequel le modèle correspond à celui spécifié, par nom, en entrée. Cette fonction est utilisée par les exemples enrollPKCS7 et enrollRenewalPKCS7.</td>
</tr>
<tr class="odd">
<td>enrollCertByTemplate</td>
<td>Initialise un objet <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> à l’aide d’un modèle, tente d’inscrire la demande de certificat créée implicitement et surveille l’état du processus d’inscription. Cette fonction est utilisée par les exemples enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 et enrollRenewalPKCS7.</td>
</tr>
<tr class="even">
<td>verifyCertContext</td>
<td>Vérifie la conformité de la chaîne de certificats par rapport à la stratégie (de base) spécifiée et, éventuellement, à l’extension d’utilisation améliorée de la clé spécifiée. Pour plus d’informations, consultez la fonction <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>CertVerifyCertificateChainPolicy</strong></a> et les structures <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> et <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> . Cette fonction est utilisée par les exemples enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 et enrollRenewalPKCS7.</td>
</tr>
<tr class="odd">
<td>decConvertFromUnicode</td>
<td>Convertit une chaîne de caractères Unicode codés sur deux octets en une chaîne de caractères ANSI sur un octet. Cette fonction est utilisée par la fonction DecodeFileW définie dans enrollCommon. cpp.</td>
</tr>
<tr class="even">
<td>DecodeFileW</td>
<td>Décode un certificat encodé ou un fichier de demande de certificat en un tableau d’octets. Cette fonction est utilisée par l’exemple installResponseFromPFX.</td>
</tr>
<tr class="odd">
<td>EncodeToFileW</td>
<td>Encode un certificat ou une demande de certificat et l’enregistre dans un fichier. Cette fonction est utilisée par les exemples createCNGCustomCMC, enrollEOBOCMC et enrollFromPublicKey.</td>
</tr>
<tr class="even">
<td>findOIDFromTemplateName</td>
<td>Récupère l’identificateur d’objet pour un modèle spécifié par nom. Cette fonction est utilisée par la fonction findCertByTemplate définie dans enrollCommon. cpp.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des exemples inclus](using-the-included-samples.md)
</dt> </dl>

 

