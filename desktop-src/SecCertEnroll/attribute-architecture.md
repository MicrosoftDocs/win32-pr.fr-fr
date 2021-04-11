---
description: Utilisé pour ajouter des attributs à une demande de certificat.
ms.assetid: 7007c751-f1a4-4ddc-a66e-d3edefc6ed97
title: Architecture des attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64d83171985c062fd2d8d4ae968c2ef4d36a29ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318957"
---
# <a name="attribute-architecture"></a>Architecture des attributs

Les interfaces suivantes sont utilisées pour ajouter des attributs à une demande de certificat :

-   [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
-   [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
-   [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
-   [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)

L’architecture suit celle définie dans le module ASN. 1 de la \# syntaxe de demande de certification PKCS 10.

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 ANY,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}
```

La collection [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) correspond au champ **attributs** , et chaque objet [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) de la collection correspond à une structure d' **attribut** ASN. 1.

Chaque **attribut** se compose d’un identificateur d’objet (OID) et de zéro ou de plusieurs valeurs associées à l’OID. Une paire OID-value unique est représentée par une interface [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) . Vous pouvez utiliser une collection [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) pour initialiser un objet [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) , mais chaque attribut de la collection doit être associé au même OID. En règle générale, un attribut n’a qu’une seule valeur.

Vous pouvez utiliser l’une des interfaces suivantes, qui dérivent de [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute), pour créer une paire d’attributs OID/value unique :

-   [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
-   [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
-   [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)
-   [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)
-   [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)
-   [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)

Par exemple, la procédure suivante montre comment créer un attribut **ClientID** .

**Pour créer un attribut **ClientID****

1.  Récupérez un objet [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) à partir d’un objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) ou [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .
2.  Créez et initialisez un objet [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) .
3.  Créez une collection [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) et ajoutez l’objet [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) .
4.  Utilisez la collection [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) pour initialiser un objet [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) .
5.  Ajoutez l’objet [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) à la collection Récupérée à l’étape 1.

L’exemple suivant illustre la sortie ASN. 1 de l’attribut **ClientID** . L’attribut contient le nom DNS de l’ordinateur sur lequel la demande a été générée (test3d.jdomcsc.nttest.microsoft.com), le nom SAM de l’utilisateur ( \\ administrateur jdomcsc) et le nom de l’application qui a généré la demande (Certreq).

``` syntax
0136: 30 57; SEQUENCE (57 Bytes)
0138: |  06 09                            ; OBJECT_ID (9 Bytes)
013a: |  |  2b 06 01 04 01 82 37 15  14
      |  |     ; 1.3.6.1.4.1.311.21.20 Client Information
0143: |  |  31 4a                         ; SET (4a Bytes)
0145: |  |     30 48                      ; SEQUENCE (48 Bytes)
0147: |  |        02 01                   ; INTEGER (1 Bytes)
0149: |  |        |  09
014a: |  |        0c 23                   ; UTF8_STRING (23 Bytes)
014c: |  |        |  74 65 73 74 33 64 2e 6a  64 6f 6d 63 73 63 2e 6e 
015c: |  |        |  74 74 65 73 74 2e 6d 69  63 72 6f 73 6f 66 74 2e 
016c: |  |        |  63 6f 6d                                         
      |  |        |     ; "test3d.jdomcsc.nttest.microsoft.com"
016f: |  |        0c 15                   ; UTF8_STRING (15 Bytes)
0171: |  |        |  4a 44 4f 4d 43 53 43 5c  61 64 6d 69 6e 69 73 74 
0181: |  |        |  72 61 74 6f 72                                   
      |  |        |     ; "JDOMCSC\administrator"
0186: |  |        0c 07                   ; UTF8_STRING (7 Bytes)
0188: |  |           63 65 72 74 72 65 71                             
      |  |              ; "certreq"
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
</dt> <dt>

[**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
</dt> <dt>

[**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
</dt> </dl>

 

 



