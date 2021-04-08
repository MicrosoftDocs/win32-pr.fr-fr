---
description: Fonctions exportées par Xenroll.dll qui peuvent être utilisées pour gérer un fournisseur de services de chiffrement.
ms.assetid: 4f6f353d-6b06-45b4-8808-56998d3727a4
title: Fonctions du fournisseur de services de chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a981b418271ba834352c0301c005b39742729a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750021"
---
# <a name="cryptographic-service-provider-functions"></a>Fonctions du fournisseur de services de chiffrement

Chacune des sections suivantes identifie une fonction exportée par Xenroll.dll qui peut être utilisée pour gérer un fournisseur de services de chiffrement. Chaque rubrique explique également comment utiliser CertEnroll.dll pour remplacer la fonction ou indique qu’il n’existe aucun mappage entre les deux bibliothèques :

-   [EnumAlgs](#enumalgs)
-   [enumContainersWStr](#enumcontainerswstr)
-   [enumProvidersWStr](#enumproviderswstr)
-   [GetAlgNameWStr](#getalgnamewstr)
-   [getProviderTypeWStr](#getprovidertypewstr)
-   [HashAlgID](#hashalgid)
-   [HashAlgorithmWStr](#hashalgorithmwstr)
-   [ProviderFlags](#providerflags)
-   [ProviderNameWStr](#providernamewstr)
-   [ProviderType](#getprovidertypewstr)
-   [Rubriques connexes](#related-topics)

## <a name="enumalgs"></a>EnumAlgs

La fonction [**EnumAlgs**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-enumalgs) dans Xenroll.dll récupère une collection d’algorithmes de chiffrement.

Lorsque vous utilisez CertEnroll.dll, vous pouvez effectuer les actions suivantes pour récupérer des informations sur les algorithmes pris en charge par un [*fournisseur de services de chiffrement*](/windows/desktop/SecGloss/c-gly) (CSP) :

1.  Appelez la propriété [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) sur un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) existant.
2.  Appelez la méthode [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) sur la requête retournée à l’étape 1 pour récupérer la requête la plus profonde.
3.  Appelez **QueryInterface** sur l’objet [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) retourné à l’étape 2 pour effectuer un cast en un objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Appelez la propriété [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) sur la \# demande PKCS 10.
5.  Appelez la propriété [**CspInformations**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_cspinformations) sur l’objet [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) récupéré à partir de l’étape 4.
6.  Appelez la propriété [**CspAlgorithms**](/windows/desktop/api/CertEnroll/nf-certenroll-icspinformation-get_cspalgorithms) sur un objet [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) spécifique dans la collection [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) Récupérée à l’étape 5.

## <a name="enumcontainerswstr"></a>enumContainersWStr

La fonction [**enumContainersWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-enumcontainerswstr) dans Xenroll.dll récupère un conteneur de clé de la collection par index.

La bibliothèque CertEnroll.dll n’implémente pas directement cette fonctionnalité.

## <a name="enumproviderswstr"></a>enumProvidersWStr

La fonction [**enumProvidersWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-enumproviderswstr) dans Xenroll.dll récupère un CSP de la collection par index.

Lorsque vous utilisez CertEnroll.dll, vous pouvez effectuer les actions suivantes pour récupérer la collection de conteneurs de chiffrement :

1.  Appelez la propriété [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) sur un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) existant.
2.  Appelez la méthode [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) sur la requête retournée à l’étape 1 pour récupérer la requête la plus profonde.
3.  Appelez **QueryInterface** sur l’objet [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) retourné à l’étape 2 pour effectuer un cast en un objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Appelez la propriété [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) sur la \# demande PKCS 10.
5.  Appelez la propriété [**CspInformations**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_cspinformations) sur l’objet [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) récupéré à partir de l’étape 4.

## <a name="getalgnamewstr"></a>GetAlgNameWStr

La fonction [**GetAlgNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getalgnamewstr) dans Xenroll.dll récupère le nom d’un [*algorithme de chiffrement*](/windows/desktop/SecGloss/c-gly).

Lorsque vous utilisez CertEnroll.dll, vous pouvez effectuer les actions suivantes pour récupérer le nom de l’algorithme :

1.  Appelez la propriété [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) sur un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) existant.
2.  Appelez la méthode [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) sur la requête retournée à l’étape 1 pour récupérer la requête la plus profonde.
3.  Appelez **QueryInterface** sur l’objet [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) retourné à l’étape 2 pour effectuer un cast en un objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Appelez la propriété [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) sur la \# demande PKCS 10.
5.  Appelez la propriété [**Algorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm) sur l’objet [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) pour récupérer l’identificateur d’objet de l’algorithme.
6.  Appelez la propriété [**FriendlyName**](/windows/desktop/api/CertEnroll/nf-certenroll-iobjectid-get_friendlyname) sur l’interface [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) pour récupérer le nom complet de l’algorithme.

## <a name="getprovidertypewstr"></a>getProviderTypeWStr

La fonction [**getProviderTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getprovidertypewstr) dans Xenroll.dll récupère le type de fournisseur de services de chiffrement.

Lorsque vous utilisez CertEnroll.dll, vous pouvez effectuer les actions suivantes pour récupérer le type de fournisseur :

1.  Appelez la propriété [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) sur un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) existant.
2.  Appelez la méthode [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) sur la requête retournée à l’étape 1 pour récupérer la requête la plus profonde.
3.  Appelez **QueryInterface** sur l’objet [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) retourné à l’étape 2 pour effectuer un cast en un objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Appelez la propriété [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) sur la \# demande PKCS 10.
5.  Appelez la propriété [**ProviderType**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providertype) sur l’objet [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) récupéré à partir de l’étape 4.

## <a name="hashalgid"></a>HashAlgID

La fonction [**HashAlgID**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_hashalgid) dans Xenroll.dll récupère une valeur entière qui contient l’ID de l’algorithme utilisé pour signer une demande.

Lorsque vous utilisez CertEnroll.dll, vous pouvez effectuer les actions suivantes pour récupérer l’algorithme de hachage :

-   Récupérez une interface [**IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) en appelant la propriété [**SignatureInformation**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_signatureinformation) sur une \# demande PKCS 10 ou CMC, ou la propriété [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) sur une demande [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) .
-   Appelez la propriété [**HashAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm) sur l’objet d’informations de signature pour récupérer l’identificateur d’objet de l’algorithme de hachage.

## <a name="hashalgorithmwstr"></a>HashAlgorithmWStr

La fonction [**HashAlgorithmWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_hashalgorithmwstr) dans Xenroll.dll spécifie ou récupère une valeur de chaîne qui identifie l’algorithme de hachage utilisé pour signer une demande.

Lorsque vous utilisez CertEnroll.dll, vous pouvez effectuer les actions suivantes pour récupérer l’algorithme de hachage :

-   Récupérez une interface [**IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) en appelant la propriété [**SignatureInformation**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_signatureinformation) sur une \# demande PKCS 10 ou CMC, ou la propriété [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) sur une \# demande PKCS 7.
-   Appelez la propriété [**HashAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm) sur l’objet d’informations de signature pour récupérer l’identificateur d’objet de l’algorithme de hachage.
-   Appelez la propriété [**FriendlyName**](/windows/desktop/api/CertEnroll/nf-certenroll-iobjectid-get_friendlyname) sur l’interface [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) retournée à l’étape 2 pour récupérer le nom complet de l’algorithme.

## <a name="providerflags"></a>ProviderFlags

La fonction [**ProviderFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providerflags) dans Xenroll.dll spécifie ou récupère les indicateurs utilisés lors de l’acquisition d’un handle vers un CSP.

La bibliothèque de CertEnroll.dll ne mappe pas parfaitement cette fonction, mais vous pouvez obtenir des informations de propriétés enrichies à partir de l’objet d’inscription et de la [*clé privée*](/windows/desktop/SecGloss/p-gly). Pour plus d’informations, examinez les propriétés exposées par les interfaces [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) et [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) .

## <a name="providernamewstr"></a>ProviderNameWStr

La fonction [**ProviderNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providernamewstr) dans Xenroll.dll spécifie ou récupère le nom d’un fournisseur de services de chiffrement.

Lorsque vous utilisez CertEnroll.dll, vous pouvez effectuer les actions suivantes pour récupérer le nom du fournisseur :

1.  Appelez la propriété [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) sur un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) existant.
2.  Appelez la méthode [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) sur la requête retournée à l’étape 1 pour récupérer la requête la plus profonde.
3.  Appelez **QueryInterface** sur l’objet [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) retourné à l’étape 2 pour effectuer un cast en un objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Appelez la propriété [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) sur la \# demande PKCS 10.
5.  Appelez la propriété [**providerName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername) sur l’objet [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) récupéré à partir de l’étape 4.

## <a name="providertype"></a>ProviderType

La fonction [**ProviderType**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providertype) dans Xenroll.dll spécifie ou récupère une valeur entière qui identifie le type du fournisseur de services de chiffrement.

Lorsque vous utilisez CertEnroll.dll, vous pouvez effectuer les actions suivantes pour récupérer le type de fournisseur :

1.  Appelez la propriété [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) sur un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) existant.
2.  Appelez la méthode [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) sur la requête retournée à l’étape 1 pour récupérer la requête la plus profonde.
3.  Appelez **QueryInterface** sur l’objet [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) retourné à l’étape 2 pour effectuer un cast en un objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Appelez la propriété [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) sur la \# demande PKCS 10.
5.  Appelez la propriété [**ProviderType**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providertype) sur l’objet [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) récupéré à partir de l’étape 4.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mappage de Xenroll.dll à CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm)
</dt> <dt>

[**ICspAlgorithms**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithms)
</dt> <dt>

[**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)
</dt> <dt>

[**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> <dt>

[**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
