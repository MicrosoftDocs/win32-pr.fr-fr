---
description: Crée une demande PKCS \# 10 personnalisée, l’envoie à une autorité de certification autonome (ca) et installe le certificat émis dans le magasin de certificats.
ms.assetid: dcb69d7e-457e-457b-9eea-15676ed710aa
title: enrollCustomPKCS10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 937b1e955ecd369794e832f16afff1594ed1df1271494d7172832132d4cb7863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780028"
---
# <a name="enrollcustompkcs10"></a>enrollCustomPKCS10

L’exemple enrollCustomPKCS10 crée une demande PKCS \# 10 personnalisée, l’envoie à une autorité de certification autonome (ca) et installe le certificat émis dans le magasin de certificats. Une autorité de certification autonome ne nécessite pas de Active Directory et n’utilise pas de modèles.

## <a name="location"></a>Emplacement

lorsque vous installez le kit de développement logiciel (SDK) de microsoft Windows, l’exemple est installé, par défaut, dans le dossier *% ProgramFiles%* \\ microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ Security \\ X509 certificate \\ \\ enrollCustomPKCS10 VC.

## <a name="discussion"></a>Discussions

Exemple enrollCustomPKCS10 :

1.  Traite les arguments de ligne de commande. La ligne de commande doit contenir le nom de l’objet du certificat X. 500, le nom de l’e-mail (RFC822) et un identificateur d’objet (OID) d’utilisation améliorée de la clé. Par exemple, vous pouvez spécifier les arguments suivants pour l’inscription *user1@example.com* :
    -   Nom de l’objet : "*CN = User1, DC = example, DC = com*"
    -   Nom du RFC822 : *user1@example.com*
    -   OID de l’authentification améliorée du client : 1.3.6.1.5.5.7.3.2
2.  Crée un objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) et l’initialise pour l’utilisateur final en spécifiant la valeur **ContextUser** de l’énumération [**X509CertificateEnrollmentContext**](/windows/desktop/api/CertEnroll/ne-certenroll-x509certificateenrollmentcontext) .
3.  Crée un objet [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , utilise l’objet pour encoder le nom du sujet en un tableau d’octets, puis ajoute le tableau à l' \# objet de requête PKCS 10.
4.  Crée un objet [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) , l’initialise à l’aide de l’identificateur d’objet (OID) EKU spécifié sur la ligne de commande, crée une collection [**IObjectIds**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectids) , ajoute le nouvel objet **IObjectId** (EKU) à la collection, utilise la collection pour initialiser un objet [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) et ajoute cet objet à la demande.
5.  Crée un objet [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) , l’initialise à l’aide du nom RFC822 spécifié sur la ligne de commande, crée une collection [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) , ajoute le nouvel objet **IAlternativeName** (nom RFC822) à la collection, crée un objet [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) et ajoute cet objet à la demande.
6.  Crée un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , l’initialise à l’aide de l’objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) et récupère une chaîne qui contient une demande encodée en base64.
7.  Crée un objet [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) et l’utilise pour récupérer une chaîne qui contient la configuration de l’autorité de certification.
8.  Crée un objet CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) et l’utilise, ainsi que les chaînes qui contiennent la configuration de l’autorité de certification et la demande de certificat pour envoyer la demande à l’autorité de certification.
9.  Vérifie l’état de l’envoi et, en cas de réussite de l’inscription, installe le certificat dans le magasin de certificats.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[\#Demande PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Utilisation des exemples inclus](using-the-included-samples.md)
</dt> </dl>

 

 
