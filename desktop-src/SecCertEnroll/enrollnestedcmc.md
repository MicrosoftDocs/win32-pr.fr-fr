---
description: Lit une demande de certificat CMC existante à partir d’un fichier, l’encapsule dans une autre demande CMC, signe cette requête externe, la soumet à une autorité de certification (CA) et enregistre la réponse du certificat de l’autorité de certification dans un fichier.
ms.assetid: b1a9161d-1f9a-4c5b-acd2-6058dc65a258
title: enrollNestedCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b55c2957fc04e8bd9a088d3a07ed10c639c29d27dd1262b34709a9215c6c8b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882939"
---
# <a name="enrollnestedcmc"></a>enrollNestedCMC

L’exemple enrollNestedCMC lit une demande de certificat CMC existante à partir d’un fichier, l’encapsule dans une autre demande CMC, signe cette requête externe, la soumet à une autorité de certification (CA) et enregistre la réponse du certificat de l’autorité de certification dans un fichier.

## <a name="location"></a>Emplacement

lorsque vous installez le kit de développement logiciel (SDK) microsoft Windows, l’exemple est installé, par défaut, dans le dossier *% ProgramFiles%* \\ microsoft sdk \\ Windows \\ v 7.0 \\ samples enrollNestedCMC de l' \\ inscription de certificats X509 \\ \\ .

## <a name="discussion"></a>Discussions

Exemple enrollNestedCMC :

1.  Traite les arguments de ligne de commande suivants :
    -   Nom du fichier d’entrée.
    -   Nom du fichier de sortie.
    -   Modèle de demande facultatif.
2.  Lit une demande CMC existante à partir d’un fichier en tant que tableau d’octets encodé base63, convertit le tableau d’octets en **BSTR**, crée un objet [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) et utilise le **BSTR** pour initialiser l’objet de requête. L’objet initialisé devient la requête interne.
3.  Utilise l’objet de requête interne créé et initialisé à l’étape précédente pour initialiser une autre demande CMC.
4.  Récupère un certificat de signature existant ou, si celui-ci est introuvable, crée une demande de certificat à partir du modèle spécifié sur la ligne de commande et tente de l’inscrire. Les fonctions findCertByTemplate et enrollCertByTemplate sont définies dans enrollCommon. cpp.
5.  Récupère la collection [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) de la demande CMC externe, crée un nouvel objet [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , l’initialise à l’aide du certificat de signature récupéré et l’ajoute à la collection.
6.  encode la demande CMC à l’aide d’Distinguished Encoding Rules (DER) et récupère la requête en tant que **BSTR**.
7.  Crée un objet [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) et l’utilise pour récupérer une chaîne qui contient la configuration de l’autorité de certification.
8.  Crée un objet CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) et l’utilise, ainsi que les chaînes qui contiennent la configuration de l’autorité de certification et la demande de certificat pour envoyer la demande à l’autorité de certification.
9.  Vérifie l’état du processus d’inscription et enregistre la réponse du certificat de l’autorité de certification dans un fichier. La fonction EncodeToFileW est définie dans enrollCommon. cpp.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Demande CMC](cmc-request.md)
</dt> <dt>

[Utilisation des exemples inclus](using-the-included-samples.md)
</dt> </dl>

 

 
