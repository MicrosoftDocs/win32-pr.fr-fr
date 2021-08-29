---
description: Crée une demande de certificat CMC pour le compte d’un autre utilisateur et inscrit l’utilisateur dans une hiérarchie de certificats.
ms.assetid: 14cc76c9-0e2b-498f-b058-244af6e9111e
title: enrollEOBOCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a9dbcddf5495f5a58d161e5bf086c737691b52312827d3420ca13a47440822
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882989"
---
# <a name="enrolleobocmc"></a>enrollEOBOCMC

L’exemple enrollEOBOCMC crée une demande de certificat CMC pour le compte d’un autre utilisateur et inscrit l’utilisateur dans une hiérarchie de certificats. L’inscription pour le compte d’un autre utilisateur nécessite que la demande de certificat soit signée à l’aide d’un certificat d’agent d’inscription.

## <a name="location"></a>Emplacement

lorsque vous installez le kit de développement logiciel (SDK) de microsoft Windows, l’exemple est installé, par défaut, dans le dossier *% ProgramFiles%* \\ microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ Security \\ X509 certificate \\ \\ enrollEOBOCMC VC.

## <a name="discussion"></a>Discussions

Exemple enrollEOBOCMC :

1.  Traite les arguments de ligne de commande suivants :
    -   Nom d’un modèle de certificat.
    -   Nom de l’utilisateur qui demande le certificat.
    -   nom d’un fichier de Exchange d’informations personnelles (PFX) dans lequel enregistrer la demande.
    -   Mot de passe à utiliser avec le fichier PFX.
    -   Nom de modèle d’agent d’inscription facultatif. Le modèle est utilisé pour créer un certificat d’agent d’inscription s’il n’en existe aucun dans le magasin de certificats.
2.  Crée un objet [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) et l’initialise à l’aide du modèle de certificat spécifié sur la ligne de commande.
3.  Ajoute le nom du demandeur à l’objet de demande CMC.
4.  Récupère un certificat d’agent d’inscription existant ou, si celui-ci est introuvable, crée une demande de certificat à partir du modèle d’agent d’inscription spécifié sur la ligne de commande et tente de l’inscrire.
5.  Vérifie la chaîne de certificats qui contient le certificat de l’agent d’inscription.
6.  Crée un objet [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , l’initialise à l’aide du certificat de l’agent d’inscription, récupère la collection [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) de l’objet de demande CMC et ajoute l’objet certificat de signature de l’agent d’inscription à la collection. L’objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) abordé à l’étape suivante utilise le certificat pour signer la demande CMC.
7.  Crée un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , l’initialise à l’aide de la demande CMC, tente de l’inscrire et vérifie la progression du processus d’inscription.
8.  Exporte le certificat installé vers un fichier PFX. Le fichier est protégé à l’aide du mot de passe spécifié sur la ligne de commande. La fonction EncodeToFileW est définie dans enrollCommon. cpp.
9.  Supprime le certificat du magasin de certificats. Les fonctions utilisées dans l’exemple de code suivant se trouvent dans la documentation CryptoAPI.
10. Supprime la clé privée de l’ordinateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Demande EOBO CMC](cmc-eobo-request.md)
</dt> <dt>

[\#Demande PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Utilisation des exemples inclus](using-the-included-samples.md)
</dt> </dl>

 

 



