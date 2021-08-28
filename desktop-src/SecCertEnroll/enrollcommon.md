---
description: Le dossier enrollCommon contient les fonctions d’assistance et les macros suivantes utilisées par les exemples fournis avec le kit de développement logiciel (SDK) d’inscription de certificats.
ms.assetid: a9b3532d-9640-4373-a6c6-7828cb6f55c7
title: enrollCommon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ddc05ad1a143de025abbc875c8280a3f419d0e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476015"
---
# <a name="enrollcommon"></a>enrollCommon

Le dossier enrollCommon contient les fonctions d’assistance et les macros suivantes utilisées par les exemples fournis avec le kit de développement logiciel (SDK) d’inscription de certificats. il est installé par défaut dans le dossier *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ Security \\ X509 certificate \\ \\ enrollCommon.




| Fonction | Description | 
|----------|-------------|
| _JumpIfError | Macro qui accepte une valeur <strong>HRESULT</strong> , une étiquette et une chaîne d’erreur, imprime la chaîne et transfère le contrôle du programme à la première instruction qui suit l’étiquette. | 
| _JumpError | Identique à la macro _JumpIfError. | 
| _PrintIfError | Pas utilisé pour l'instant. | 
| _PrintError | Macro qui imprime un message d’erreur et une valeur <strong>HRESULT</strong> . | 
| convertWszToSz | Convertit une chaîne de caractères larges en une chaîne de caractères ASCII à l’aide de la fonction <strong>WideCharToMultiByte</strong> et de l’identificateur de page de codes ANSI actuel du système. Cette fonction est utilisée par les fonctions decConvertFromUnicode et findOIDFromTemplateName définies dans enrollCommon. cpp. | 
| convertSzToWsz | Convertit une chaîne ASCII en une chaîne de caractères larges à l’aide de la fonction <strong>MultiByteToWideChar</strong> et de l’identificateur de page de codes ANSI actuel du système. Cette fonction est utilisée par la fonction findCertByTemplate définie dans enrollCommon. cpp. | 
| convertSzToBstr | Convertit une chaîne ASCII en <strong>BSTR</strong> à l’aide de la fonction <strong>MultiByteToWideChar</strong> . Cette fonction n’est pas utilisée actuellement. | 
| convertWszToBstr | Convertit une chaîne de caractères larges en <strong>BSTR</strong>. Cette fonction est utilisée par l’exemple installResponseFromPFX. | 
| checkEnrollStatus | Vérifie l’état du processus d’inscription de certificats à l’aide des interfaces <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> et <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus</strong></a> . Cette fonction est utilisée par les exemples enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert et enrollSimpleUserCert. | 
| findCertByKeyUsage | Énumère le magasin de certificats personnels de l’utilisateur actuel pour rechercher le premier certificat pour lequel l’utilisation prévue de la clé publique correspond à une valeur spécifiée. La valeur spécifiée peut être une combinaison au niveau du bit des indicateurs suivants :<ul><li>CERT_DATA_ENCIPHERMENT_KEY_USAGE</li><li>CERT_DIGITAL_SIGNATURE_KEY_USAGE</li><li>CERT_KEY_AGREEMENT_KEY_USAGE</li><li>CERT_KEY_CERT_SIGN_KEY_USAGE</li><li>CERT_KEY_ENCIPHERMENT_KEY_USAGE</li><li>CERT_NON_REPUDIATION_KEY_USAGE</li><li>CERT_OFFLINE_CRL_SIGN_KEY_USAGE</li></ul>Cette fonction est utilisée par l’exemple enrollFromPublicKey.<br /> | 
| findCertByEKU | Énumère le magasin de certificats personnels de l’utilisateur actuel pour rechercher le premier certificat pour lequel l’extension d’utilisation améliorée de la clé correspond à celle spécifiée en entrée. Pour plus d’informations sur l’extension d’utilisation améliorée de la carte, consultez l’interface <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage</strong></a> . Cette fonction est utilisée par l’exemple enrollEOBOCMC. | 
| findCertByTemplate | Énumère le magasin de certificats personnels de l’utilisateur actuel pour rechercher le premier certificat pour lequel le modèle correspond à celui spécifié, par nom, en entrée. Cette fonction est utilisée par les exemples enrollPKCS7 et enrollRenewalPKCS7. | 
| enrollCertByTemplate | Initialise un objet <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> à l’aide d’un modèle, tente d’inscrire la demande de certificat créée implicitement et surveille l’état du processus d’inscription. Cette fonction est utilisée par les exemples enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 et enrollRenewalPKCS7. | 
| verifyCertContext | Vérifie la conformité de la chaîne de certificats par rapport à la stratégie (de base) spécifiée et, éventuellement, à l’extension d’utilisation améliorée de la clé spécifiée. Pour plus d’informations, consultez la fonction <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>CertVerifyCertificateChainPolicy</strong></a> et les structures <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> et <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> . Cette fonction est utilisée par les exemples enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 et enrollRenewalPKCS7. | 
| decConvertFromUnicode | Convertit une chaîne de caractères Unicode codés sur deux octets en une chaîne de caractères ANSI sur un octet. Cette fonction est utilisée par la fonction DecodeFileW définie dans enrollCommon. cpp. | 
| DecodeFileW | Décode un certificat encodé ou un fichier de demande de certificat en un tableau d’octets. Cette fonction est utilisée par l’exemple installResponseFromPFX. | 
| EncodeToFileW | Encode un certificat ou une demande de certificat et l’enregistre dans un fichier. Cette fonction est utilisée par les exemples createCNGCustomCMC, enrollEOBOCMC et enrollFromPublicKey. | 
| findOIDFromTemplateName | Récupère l’identificateur d’objet pour un modèle spécifié par nom. Cette fonction est utilisée par la fonction findCertByTemplate définie dans enrollCommon. cpp. | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des exemples inclus](using-the-included-samples.md)
</dt> </dl>

 

