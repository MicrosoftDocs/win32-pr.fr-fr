---
description: Les propriétés sont utilisées pour associer une valeur à un certificat.
ms.assetid: a6433416-fe77-4bb0-bd8e-9410a49ab861
title: Fonctions de propriété externes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40196f4f42823ad44debeccc0fa85dc4615d58d1a0ccf521b2dd796e72574db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117779629"
---
# <a name="external-property-functions"></a>Fonctions de propriété externes

Les propriétés sont utilisées pour associer une valeur à un certificat. Les propriétés ne sont jamais envoyées ni traitées par une [*autorité de certification*](/windows/desktop/SecGloss/c-gly) (ca) et ne sont pas stockées dans un certificat. En règle générale, ils sont associés à un certificat une fois que le certificat a été reçu de l’autorité de certification et avant qu’il ne soit enregistré dans un magasin. Les propriétés sont enregistrées dans le magasin avec le certificat. CertEnroll.dll implémente l’interface [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) et les interfaces suivantes dérivées de **ICertProperty**:

-   [**ICertPropertyArchived**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchived)
-   [**ICertPropertyArchivedKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchivedkeyhash)
-   [**ICertPropertyAutoEnroll**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyautoenroll)
-   [**ICertPropertyBackedUp**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertybackedup)
-   [**ICertPropertyDescription**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertydescription)
-   [**ICertPropertyEnrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyenrollment)
-   [**ICertPropertyFriendlyName**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyfriendlyname)
-   [**ICertPropertyKeyProvInfo**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertykeyprovinfo)
-   [**ICertPropertyRenewal**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrenewal)
-   [**ICertPropertyRequestOriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)
-   [**ICertPropertySHA1Hash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertysha1hash)

Chacune des sections suivantes identifie une fonction exportée par Xenroll.dll pour gérer les propriétés d’un certificat externe. Chaque section explique également comment utiliser CertEnroll.dll pour remplacer la fonction ou indique qu’il n’existe aucun mappage entre les deux bibliothèques :

-   [addBlobPropertyToCertificateWStr](#addblobpropertytocertificatewstr)
-   [GetPrivateKeyArchiveCertificate](#getprivatekeyarchivecertificate)
-   [resetBlobProperties](#resetblobproperties)
-   [SetPrivateKeyArchiveCertificate](#setprivatekeyarchivecertificate)
-   [SetSignerCertificate](#setsignercertificate)
-   [ThumbPrintWStr](#thumbprintwstr)
-   [Rubriques connexes](#related-topics)

## <a name="addblobpropertytocertificatewstr"></a>addBlobPropertyToCertificateWStr

La fonction [**addBlobPropertyToCertificateWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addblobpropertytocertificatewstr) dans Xenroll.dll ajoute une propriété au certificat.

Dans CertEnroll.dll, tous les objets dérivés de [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) implémentent une méthode [**SetValueOnCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-icertproperty-setvalueoncertificate) que vous pouvez utiliser pour associer une propriété à un certificat. En outre, l’objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) implémente directement les propriétés [**CertificateFriendlyName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificatefriendlyname) et [**CertificateDescription**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificatedescription) .

## <a name="getprivatekeyarchivecertificate"></a>GetPrivateKeyArchiveCertificate

La fonction [**GetPrivateKeyArchiveCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getprivatekeyarchivecertificate) dans Xenroll.dll récupère le certificat Exchange utilisé pour archiver une [*clé privée*](/windows/desktop/SecGloss/p-gly).

Vous pouvez utiliser l’objet [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) dans CertEnroll.dll pour créer une demande d’archivage de votre clé privée par une autorité de certification. Vous devez récupérer un certificat Exchange auprès de l’autorité de certification et utiliser la [*clé publique*](/windows/desktop/SecGloss/p-gly) contenue dans ce certificat pour chiffrer la clé privée que vous soumettez pour l’archivage. Pour spécifier ou récupérer un certificat d’échange d’autorité de certification, appelez la propriété [**KeyArchivalCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_keyarchivalcertificate) sur cet objet.

## <a name="resetblobproperties"></a>resetBlobProperties

La fonction [**resetBlobProperties**](/windows/desktop/api/xenroll/nf-xenroll-icenroll4-resetblobproperties) dans Xenroll.dll supprime la collection de propriétés du certificat.

Dans CertEnroll.dll, tous les objets Property dérivés de [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) implémentent la propriété [**RemoveFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-icertproperty-removefromcertificate) que vous pouvez utiliser pour dissocier une propriété d’un certificat.

## <a name="setprivatekeyarchivecertificate"></a>SetPrivateKeyArchiveCertificate

La fonction [**SetPrivateKeyArchiveCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setprivatekeyarchivecertificate) dans Xenroll.dll spécifie un certificat Exchange utilisé pour archiver une clé privée.

Vous pouvez utiliser l’objet [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) dans CertEnroll.dll pour créer une demande d’archivage de votre clé privée par une autorité de certification. Vous devez récupérer un certificat Exchange auprès de l’autorité de certification et utiliser la clé publique contenue dans ce certificat pour chiffrer la clé privée que vous soumettez pour l’archivage. Pour spécifier ou récupérer un certificat d’échange d’autorité de certification, appelez la propriété [**KeyArchivalCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_keyarchivalcertificate) sur cet objet.

## <a name="setsignercertificate"></a>SetSignerCertificate

La fonction [**SetSignerCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setsignercertificate) dans Xenroll.dll spécifie un certificat de signataire.

L’objet [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) dans CertEnroll.dll peut être utilisé pour signer une [*demande de certificat*](/windows/desktop/SecGloss/c-gly) [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly), CMC ou auto-signé. Vous pouvez initialiser l’objet à l’aide d’un certificat de signature existant et l’associer à une demande en appelant l’une des propriétés suivantes :

-   [**SignerCertificates**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_signercertificates) sur [ **IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
-   [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) sur [ **IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
-   [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcertificate-get_signercertificate) sur [ **IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)

En outre, si vous initialisez une demande CMC à partir d’une requête interne et d’un modèle, ou que vous initialisez une \# demande PKCS 7 à partir d’une demande existante, le certificat de signature peut être défini.

## <a name="thumbprintwstr"></a>ThumbPrintWStr

La fonction [**ThumbPrintWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_thumbprintwstr) dans Xenroll.dll spécifie ou récupère la valeur du hachage du certificat.

Dans CertEnroll.dll, vous pouvez utiliser l’objet [**ICertPropertySHA1Hash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertysha1hash) pour récupérer une valeur de [*hachage*](/windows/desktop/SecGloss/h-gly) ([*empreinte numérique*](/windows/desktop/SecGloss/t-gly)) créée en appelant la méthode [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mappage de Xenroll.dll à CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

 
