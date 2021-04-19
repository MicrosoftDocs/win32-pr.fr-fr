---
description: Le format de certificat X. 509 version 3 identifie plusieurs extensions qui peuvent être ajoutées à un certificat pour fournir des informations améliorées sur l’utilisation de la clé, les stratégies de certificat et les contraintes, les autres formats de nom, et bien plus encore.
ms.assetid: d53107b7-a153-41cf-9876-1d28aaf99816
title: Fonctions d’extension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bc490c8763a00fae9e7fb1e8a702ff87e2c18fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520655"
---
# <a name="extension-functions"></a>Fonctions d’extension

Le format de certificat [*X. 509*](/windows/desktop/SecGloss/x-gly) version 3 identifie plusieurs extensions qui peuvent être ajoutées à un certificat pour fournir des informations améliorées sur l’utilisation de la clé, les stratégies de certificat et les contraintes, les autres formats de nom, et bien plus encore.

CertEnroll.dll implémente les interfaces suivantes pour gérer les extensions de certificat :

-   [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)
-   [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
-   [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)
-   [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)
-   [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)
-   [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)
-   [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)
-   [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)
-   [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)
-   [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)
-   [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)
-   [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)
-   [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)

Chacune des sections suivantes traite d’une fonction exportée par Xenroll.dll pour gérer les extensions de certificat. Chaque section explique également comment utiliser CertEnroll.dll pour remplacer la fonction ou indique qu’il n’existe aucun mappage entre les deux bibliothèques :

-   [AddCertTypeToRequestWStr](#addcerttypetorequestwstr)
-   [AddCertTypeToRequestWStrEx](#addcerttypetorequestwstrex)
-   [AddExtensionsToRequest](#addextensionstorequest)
-   [addExtensionToRequestWStr](#addextensiontorequestwstr)
-   [EnableSMIMECapabilities](#enablesmimecapabilities)
-   [IncludeSubjectKeyID](#includesubjectkeyid)
-   [resetExtensions](#resetextensions)
-   [Rubriques connexes](#related-topics)

## <a name="addcerttypetorequestwstr"></a>AddCertTypeToRequestWStr

La fonction [**AddCertTypeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addcerttypetorequestwstr) dans Xenroll.dll ajoute un modèle de certificat, par son nom, à une demande.

À l’aide de CertEnroll.dll, la méthode recommandée pour incorporer un modèle dans une demande de certificat consiste à utiliser la méthode [**InitializeFromTemplateName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromtemplatename) sur un \# objet de requête PKCS 10 ou [* PKCS] ou la méthode [**INITIALIZEFROMINNERREQUESTTEMPLATENAME**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-initializefrominnerrequesttemplatename) sur une demande CMC.

Si un modèle spécifique n’est pas disponible sur le client, mais qu’il doit être compris par l' [*autorité de certification*](/windows/desktop/SecGloss/c-gly) , vous pouvez utiliser l’interface [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) pour ajouter un modèle de version 1 ou vous pouvez utiliser l’interface [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate) pour ajouter un modèle de version 2 à une demande de certificat. Par exemple, pour ajouter un modèle de version 1, effectuez les actions suivantes :

1.  Créez un objet [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .
2.  Créez un objet [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) et appelez la méthode [**InitializeEncode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensiontemplatename-initializeencode) , en spécifiant le nom du modèle.
3.  Ajoutez l’extension créée à la collection [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) en appelant la méthode [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add) .
4.  Créez un objet [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) et appelez la méthode [**InitializeEncode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributeextensions-initializeencode) , en spécifiant la collection [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) en entrée.
5.  Récupérez un objet de collection [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) en appelant la propriété [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) sur un objet de requête [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) ou [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) existant.

## <a name="addcerttypetorequestwstrex"></a>AddCertTypeToRequestWStrEx

La fonction [**AddCertTypeToRequestWStrEx**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addcerttypetorequestwstrex) dans Xenroll.dll ajoute un modèle de certificat à une demande par son nom, son identificateur d’objet et sa version.

Pour plus d’informations sur l’utilisation de CertEnroll.dll pour incorporer des informations de modèle dans une demande, consultez AddCertTypeToRequestWStr.

## <a name="addextensionstorequest"></a>AddExtensionsToRequest

La fonction [**AddExtensionsToRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addextensionstorequest) dans Xenroll.dll ajoute une collection d’extensions à une demande.

Dans CertEnroll.dll, les extensions sont ajoutées à la collection d’attributs d’une demande CMC ou PKCS \# 10. Pour ajouter des extensions, effectuez les actions suivantes :

1.  Créez un objet [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .
2.  Créez un objet [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) et appelez la méthode [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extension-initialize) pour créer une extension à partir d’un identificateur d’objet et d’une valeur d’extension, ou utilisez l’une des interfaces répertoriées précédemment pour définir l’une des extensions les plus courantes.
3.  Ajoutez chaque nouvelle extension créée à l’étape précédente à la collection [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) en appelant la méthode [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add) .

## <a name="addextensiontorequestwstr"></a>addExtensionToRequestWStr

La fonction [**addExtensionToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addextensiontorequestwstr) dans Xenroll.dll ajoute une extension spécifique à la demande.

Dans CertEnroll.dll, une extension spécifique doit être définie et ajoutée à une collection d’extensions avant que la collection d’extensions soit ajoutée à la collection d’attributs d’une demande CMC ou PKCS \# 10. Pour plus d’informations, consultez la discussion AddExtensionsToRequest ci-dessus.

## <a name="enablesmimecapabilities"></a>EnableSMIMECapabilities

La fonction [**EnableSMIMECapabilities**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_enablesmimecapabilities) dans Xenroll.dll spécifie ou récupère une valeur booléenne qui indique s’il faut ajouter l’extension **SMIMECapabilities** à la demande.

Vous pouvez appeler la propriété [**SmimeCapabilities**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_smimecapabilities) sur l’objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) pour ajouter automatiquement un objet [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities) à la demande avant l’encodage.

## <a name="includesubjectkeyid"></a>IncludeSubjectKeyID

La fonction [**IncludeSubjectKeyID**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_includesubjectkeyid) dans Xenroll.dll spécifie ou récupère une valeur booléenne qui indique s’il faut ajouter l’extension **extension SubjectKeyIdentifier** à la demande.

Par défaut, l’extension **extension SubjectKeyIdentifier** est créée lorsque l’objet de requête [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) est initialisé. Vous pouvez remplacer ce comportement en appelant la propriété [**SuppressOids**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_suppressoids) .

Si vous disposez d’une [*paire de clés publique/privée*](/windows/desktop/SecGloss/p-gly), vous pouvez également utiliser l’interface [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier) dans CertEnroll.dll pour ajouter une extension **extension SubjectKeyIdentifier** à une demande de certificat en effectuant les actions suivantes :

1.  Créez un objet [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .
2.  Créez un objet [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier) et appelez la méthode [**InitializeEncode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensionsubjectkeyidentifier-initializeencode) , en spécifiant une chaîne qui contient l’identificateur. En règle générale, il s’agit d’un hachage SHA-1 de 20 octets de la [*clé publique*](/windows/desktop/SecGloss/p-gly) contenue dans le certificat de signature de l’autorité de certification.
3.  Ajoutez l’extension créée à la collection [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) en appelant la méthode [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-add) .
4.  Créez un objet [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) et appelez la méthode [**InitializeEncode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributeextensions-initializeencode) , en spécifiant la collection [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) en entrée.
5.  Récupérez un objet de collection [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) en appelant la propriété [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) sur un objet de requête [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) ou [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) existant.

## <a name="resetextensions"></a>resetExtensions

La fonction [**resetExtensions**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetextensions) dans Xenroll.dll supprime la collection d’extensions de la demande.

Pour supprimer une extension d’une requête par numéro d’index à l’aide de CertEnroll.dll, appelez la méthode [**Remove**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-remove) sur la collection [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) . Pour supprimer tous les attributs d’une requête, appelez la méthode [**Clear**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509extensions-clear) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mappage de Xenroll.dll à CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)
</dt> <dt>

[**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)
</dt> </dl>

 

 
