---
description: Des attributs peuvent être ajoutés à une demande de certificat pour fournir à une autorité de certification (CA) des informations supplémentaires qu’il peut utiliser lors de la création et de l’émission d’un certificat.
ms.assetid: 3eba5a2f-eeac-4e38-8705-b12bc183b7eb
title: Fonctions d’attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a353b5beb5b7da048edf8712c5d82545fd326a7d1720748705ae093aaa2cc44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903111"
---
# <a name="attribute-functions"></a>Fonctions d’attribut

Des attributs peuvent être ajoutés à une demande de certificat pour fournir à une [*autorité de certification*](/windows/desktop/SecGloss/c-gly) (ca) des informations supplémentaires qu’il peut utiliser lors de la création et de l’émission d’un certificat.

CertEnroll.dll implémente les interfaces suivantes pour définir des attributs et des collections d’attributs :

-   [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
-   [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
-   [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
-   [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
-   [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
-   [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
-   [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)
-   [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)
-   [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)
-   [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)

Les sections suivantes identifient les fonctions exportées par Xenroll.dll pour associer des attributs de chiffrement à des demandes de certificat et expliquent comment utiliser CertEnroll.dll pour remplacer la fonction ou indiquer qu’il n’existe aucun mappage entre les deux bibliothèques :

-   [addAttributeToRequestWStr](#addattributetorequestwstr)
-   [AddAuthenticatedAttributesToPKCS7Request](#addauthenticatedattributestopkcs7request)
-   [addNameValuePairToRequestWStr](#addnamevaluepairtorequestwstr)
-   [AddNameValuePairToSignatureWStr](#addnamevaluepairtosignaturewstr)
-   [ClientId](#clientid)
-   [RenewalCertificate](#renewalcertificate)
-   [resetAttributes](#resetattributes)
-   [Rubriques connexes](#related-topics)

## <a name="addattributetorequestwstr"></a>addAttributeToRequestWStr

La fonction [**addAttributeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) dans Xenroll.dll ajoute un attribut à une demande de certificat.

En général, pour ajouter un attribut à une requête à l’aide des objets implémentés dans CertEnroll.dll, vous pouvez effectuer les actions suivantes :

1.  Créez un objet de collection [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) .
2.  Créez un objet [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) et appelez la méthode [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attribute-initialize) pour créer un attribut à partir d’un identificateur d’objet et d’une valeur d’attribut, ou utilisez l’une des interfaces répertoriées précédemment pour définir l’un des attributs les plus courants.
3.  Ajoutez chaque nouvel attribut créé à l’étape précédente à la collection [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) à l’aide de la méthode [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-add) .
4.  Créez un objet [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) et initialisez-le en appelant la méthode [**InitializeFromValues**](/windows/desktop/api/CertEnroll/nf-certenroll-icryptattribute-initializefromvalues) et en spécifiant la collection [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) en entrée.
5.  Récupérez un objet de collection [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) en appelant la propriété [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) sur un objet de requête [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) ou [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) existant.
6.  Ajoutez l’objet [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) à la collection [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) .

## <a name="addauthenticatedattributestopkcs7request"></a>AddAuthenticatedAttributesToPKCS7Request

Les attributs authentifiés sont des paires nom-valeur qui sont signées par et ajoutées à une signature. La fonction [**AddAuthenticatedAttributesToPKCS7Request**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addauthenticatedattributestopkcs7request) dans Xenroll.dll ajoute un tableau d’attributs authentifiés à une demande [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) .

Comme indiqué ci-dessus pour la fonction [**addAttributeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) , vous pouvez utiliser CertEnroll.dll pour définir facilement et ajouter une collection d’attributs à une demande de certificat. Toutefois, vous ne pouvez pas choisir si l’attribut est authentifié. Le processus d’inscription prend automatiquement cette décision.

## <a name="addnamevaluepairtorequestwstr"></a>addNameValuePairToRequestWStr

La fonction [**addNameValuePairToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addnamevaluepairtorequestwstr) dans Xenroll.dll ajoute une paire nom-valeur non authentifiée à une demande.

Vous pouvez utiliser l’interface [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) dans CertEnroll.dll pour définir une paire nom-valeur, et vous pouvez ajouter une collection de paires nom-valeur à un objet de demande CMC en effectuant les actions suivantes :

1.  Créez et initialisez un objet [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) . Le processus d’initialisation crée une collection [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) vide.
2.  Appelez la propriété [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) sur un objet de demande CMC existant pour récupérer la collection.
3.  Créez et initialisez un objet [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) .
4.  Ajoutez chaque nouvelle paire nom-valeur à la collection [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) en appelant la méthode [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509namevaluepairs-add) .

Le processus d’inscription place la collection de paires nom-valeur dans la structure **TaggedAttribute** de la demande CMC.

## <a name="addnamevaluepairtosignaturewstr"></a>AddNameValuePairToSignatureWStr

La fonction [**AddNameValuePairToSignatureWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addnamevaluepairtosignaturewstr) dans Xenroll.dll ajoute une paire nom-valeur authentifiée à une demande. Cette valeur est généralement utilisée pour spécifier le nom du demandeur dans une demande d’inscription (EOBO).

Dans CertEnroll.dll, utilisez la propriété [**RequesterName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_requestername) pour spécifier le nom dans une demande EOBO.

## <a name="clientid"></a>ClientId

La fonction [**ClientID**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_clientid) dans Xenroll.dll spécifie ou récupère un attribut **ClientID** .

Utilisez la propriété [**ClientID**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_clientid) dans CertEnroll.dll pour ajouter cet attribut à une demande CMC ou PKCS \# 10.

## <a name="renewalcertificate"></a>RenewalCertificate

La fonction [**RenewalCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_renewalcertificate) dans Xenroll.dll spécifie ou récupère un attribut **RenewalCertificate** .

Dans CertEnroll.dll, quand vous appelez [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) sur un \# objet PKCS 7 ou PKCS) est automatiquement créé.

## <a name="resetattributes"></a>resetAttributes

La fonction [**resetAttributes**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetattributes) dans Xenroll.dll supprime la collection d’attributs d’une demande.

Pour supprimer un attribut d’une requête par index à l’aide de CertEnroll.dll, appelez la méthode [**Remove**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-remove) sur la collection [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) . Pour supprimer tous les attributs d’une requête, appelez la méthode [**Clear**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-clear) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mappage de Xenroll.dll à CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
</dt> <dt>

[**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
</dt> <dt>

[**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
</dt> <dt>

[**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)
</dt> <dt>

[**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)
</dt> </dl>

 

 
