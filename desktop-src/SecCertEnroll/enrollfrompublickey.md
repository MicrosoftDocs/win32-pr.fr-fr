---
description: Initialise un objet de \# demande de certificat PKCS 10, l’encapsule dans un objet de demande CMC, soumet la demande CMC à une autorité de certification d’entreprise (ca) et enregistre le certificat retourné par l’autorité de certification dans un fichier.
ms.assetid: 0231da3b-a183-4443-8735-5affd24b145a
title: enrollFromPublicKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0346e2966dc9109ed9413022ead4eda487c37c2ac66ad9da42d2dcee2445032
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780048"
---
# <a name="enrollfrompublickey"></a>enrollFromPublicKey

L’exemple enrollFromPublicKey Initialise un objet de \# demande de certificat PKCS 10, l’encapsule dans un objet de demande CMC, soumet la demande CMC à une autorité de certification d’entreprise (ca) et enregistre le certificat retourné par l’autorité de certification dans un fichier.

## <a name="location"></a>Emplacement

lorsque vous installez le kit de développement logiciel (SDK) de microsoft Windows, l’exemple est installé, par défaut, dans le dossier *% ProgramFiles%* \\ microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ Security \\ X509 certificate \\ \\ enrollFromPublicKey VC.

## <a name="discussion"></a>Discussions

Exemple enrollFromPublicKey :

1.  Traite les arguments de ligne de commande suivants :
    -   Nom d’un modèle de certificat.
    -   Nom d’un fichier dans lequel enregistrer le certificat installé sous la forme d’un tableau d’octets encodé en base64.
    -   Nom de modèle de certificat de signature facultatif. Le modèle est utilisé pour créer un certificat de signature s’il n’en existe aucun dans le magasin de certificats.
2.  Crée un objet de clé privée [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) et appelle la méthode [**Create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create) pour créer une clé privée asymétrique à l’aide du fournisseur de services de chiffrement par défaut, de la taille de la clé et des valeurs [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) pour l’ordinateur actuel.
3.  Récupère la partie clé publique de l’objet [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) .
4.  Crée un objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) et l’initialise à l’aide du modèle spécifié sur la ligne de commande et de la clé publique.
5.  Crée un objet [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) et l’initialise à l’aide de l' \# objet de requête PKCS 10.
6.  Récupère un certificat de signature existant ou, si celui-ci est introuvable, crée une demande de certificat à partir du modèle spécifié sur la ligne de commande et tente de l’inscrire. FindCertByKeyUsage est défini dans enrollCommon. cpp.
7.  Vérifie la chaîne de certificats.
8.  Crée un objet [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , l’initialise à l’aide du certificat de signature, récupère la collection [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) de l’objet de demande CMC et ajoute l’objet de certificat de signature à la collection.
9.  encode la demande CMC à l’aide d' [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER).
10. Crée un objet [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) et l’utilise pour récupérer une chaîne qui contient la configuration de l’autorité de certification.
11. Crée un objet CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) et l’utilise, ainsi que les chaînes qui contiennent la configuration de l’autorité de certification et la demande de certificat pour envoyer la demande à l’autorité de certification.
12. Vérifie l’état du processus d’inscription et enregistre le certificat installé dans un fichier. La fonction EncodeToFileW est définie dans enrollCommon. cpp.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Demande CMC](cmc-request.md)
</dt> <dt>

[\#Demande PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Utilisation des exemples inclus](using-the-included-samples.md)
</dt> </dl>

 

 
