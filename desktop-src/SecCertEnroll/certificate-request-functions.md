---
description: La bibliothèque CertEnroll.dll implémente cinq interfaces qui peuvent être utilisées pour créer et gérer une demande de certificat.
ms.assetid: f4630095-6ba2-46f7-8825-e7a5b1cb185a
title: Fonctions de demande de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e07fb348b335562863f04226a2fb729bfbcbdaba27cb574a04c87075a64653a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902568"
---
# <a name="certificate-request-functions"></a>Fonctions de demande de certificat

La bibliothèque CertEnroll.dll implémente cinq interfaces qui peuvent être utilisées pour créer et gérer une demande de certificat. Parmi celles-ci, l’interface [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) représente un objet de base abstrait qui définit des signatures de méthode héritées par les quatre interfaces suivantes.

| Interface                                                                        | Description                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | Vous permet de créer directement un certificat sans l’appliquer à une [*autorité de certification*](/windows/desktop/SecGloss/c-gly) (ca).<br/>                                                                                                            |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | Représente une demande de certificat [*gestion des certificats par le biais du MCG*](/windows/desktop/SecGloss/c-gly) (certificat de gestion des certificats sur CMS) qui peut contenir une requête PKCS 10 imbriquée \# ou un autre objet de demande CMC.<br/> |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | Représente un objet de demande de syntaxe de message de certificat [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) qui doit contenir une requête PKCS \# 10 imbriquée.<br/>                                                                                                         |
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | Représente une \# demande de certificat PKCS 10. Une \# requête PKCS 10 peut être envoyée directement à une autorité de certification, ou elle peut être encapsulée par une \# demande PKCS 7 ou CMC.<br/>                                                                                                                                                            |



 

Vous pouvez utiliser un objet de demande de certificat pour initialiser un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) pour inscrire un client dans une hiérarchie de certificats et installer la réponse de certificat retournée par l’autorité de certification.

Chacune des sections suivantes identifie une fonction exportée par Xenroll.dll pour créer, énumérer ou supprimer des demandes de certificat. Chaque section explique également comment utiliser CertEnroll.dll pour remplacer la fonction ou indique qu’il n’existe aucun mappage entre les deux bibliothèques :

-   [createFilePKCS10WStr](#createfilepkcs10wstr)
-   [createFileRequestWStr](#createfilerequestwstr)
-   [createPKCS10WStr](#createpkcs10wstr)
-   [CreatePKCS7RequestFromRequest](#createpkcs7requestfromrequest)
-   [createRequestWStr](#createrequestwstr)
-   [DeleteRequestCert](#deleterequestcert)
-   [enumPendingRequestWStr](#enumpendingrequestwstr)
-   [removePendingRequestWStr](#removependingrequestwstr)
-   [Réinitialiser](#reset)
-   [setPendingRequestInfoWStr](#setpendingrequestinfowstr)
-   [Rubriques connexes](#related-topics)

## <a name="createfilepkcs10wstr"></a>createFilePKCS10WStr

La fonction [**createFilePKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr) dans Xenroll.dll crée une demande de certificat PKCS 10 encodée en base64 \# et l’enregistre dans un fichier.

La bibliothèque CertEnroll.dll n’implémente pas directement les fonctionnalités permettant d’écrire une requête dans un fichier. Toutefois, vous pouvez récupérer une demande de certificat en appelant la propriété [**rawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata) sur l’objet [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) et en créant une fonction personnalisée pour copier la valeur dans un fichier.

## <a name="createfilerequestwstr"></a>createFileRequestWStr

La fonction [**createFileRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilerequestwstr) dans Xenroll.dll crée une \# demande de certificat PKCS 7, PKCS \# 10 ou CMC et l’enregistre dans un fichier.

La bibliothèque CertEnroll.dll n’implémente pas directement les fonctionnalités permettant d’écrire une requête dans un fichier. Toutefois, vous pouvez récupérer une demande de certificat en appelant la propriété [**rawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata) sur l’objet [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) et en créant une fonction personnalisée pour copier la valeur dans un fichier.

## <a name="createpkcs10wstr"></a>createPKCS10WStr

La fonction [**createPKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr) dans Xenroll.dll crée une \# demande de certificat PKCS 10 et la copie dans un tableau d’octets.

Vous pouvez utiliser un objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) pour initialiser une \# requête PKCS 10 à partir d’une demande existante, d’un certificat existant, d’une [*clé privée*](/windows/desktop/SecGloss/p-gly), d’une [*clé publique*](/windows/desktop/SecGloss/p-gly)ou d’un modèle.

## <a name="createpkcs7requestfromrequest"></a>CreatePKCS7RequestFromRequest

La fonction [**CreatePKCS7RequestFromRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs7requestfromrequest) dans Xenroll.dll crée une \# demande de certificat PKCS 7 et la copie dans un tableau d’octets.

Vous pouvez utiliser un objet [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) pour initialiser une \# demande PKCS 7 à partir d’une demande existante, d’un certificat existant, d’un objet de requête interne ou d’un modèle.

## <a name="createrequestwstr"></a>createRequestWStr

La fonction [**createRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createrequestwstr) dans Xenroll.dll crée une \# demande de certificat PKCS 7, PKCS \# 10 ou CMC et la copie dans un tableau d’octets.

Pour utiliser la bibliothèque de CertEnroll.dll pour créer \# des demandes PKCS 7, PKCS \# 10 ou CMC, vous pouvez créer et initialiser des instances des objets [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7), [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)ou [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .

## <a name="deleterequestcert"></a>DeleteRequestCert

La fonction [**DeleteRequestCert**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_deleterequestcert) dans Xenroll.dll spécifie ou récupère une valeur booléenne qui indique si un certificat fictif est supprimé après l’installation d’une réponse de certificat.

L’objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) dans CertEnroll.dll crée automatiquement des certificats factices dans le magasin de demandes pour enregistrer temporairement diverses propriétés de certificat qui sont initialisées lors du processus d’inscription. Une fois qu’un certificat a été émis par une autorité de certification, les propriétés sont copiées dans le nouveau certificat et le certificat factice est supprimé. La bibliothèque de CertEnroll.dll ne vous permet pas de forcer un certificat factice à rester après l’installation de la réponse du certificat.

## <a name="enumpendingrequestwstr"></a>enumPendingRequestWStr

La fonction [**enumPendingRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-enumpendingrequestwstr) dans Xenroll.dll récupère une valeur de propriété spécifiée pour une demande en attente.

La bibliothèque de CertEnroll.dll n’implémente pas directement les fonctionnalités de suppression d’une demande de certificat en attente.

## <a name="removependingrequestwstr"></a>removePendingRequestWStr

La fonction [**removePendingRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-removependingrequestwstr) dans Xenroll.dll supprime une demande en attente du magasin de demandes.

La bibliothèque de CertEnroll.dll n’implémente pas directement les fonctionnalités de suppression d’une demande de certificat en attente.

## <a name="reset"></a>Réinitialiser

La fonction [**Reset**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-reset) dans Xenroll.dll retourne le contrôle d’inscription de certificat à un état initial.

Vous pouvez obtenir le même résultat en utilisant Certenroll.dll pour créer un nouvel objet de requête du type requis.

## <a name="setpendingrequestinfowstr"></a>setPendingRequestInfoWStr

La fonction [**setPendingRequestInfoWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setpendingrequestinfowstr) dans Xenroll.dll spécifie les propriétés de la demande en attente.

La bibliothèque de CertEnroll.dll n’implémente pas directement les fonctionnalités de suppression d’une demande de certificat en attente. Vous pouvez appeler la propriété [**CAConfigString**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_caconfigstring) sur l’objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) pour récupérer une chaîne de configuration, mais uniquement pour un objet d’inscription actif.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mappage de Xenroll.dll à CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)
</dt> <dt>

[**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)
</dt> <dt>

[**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

