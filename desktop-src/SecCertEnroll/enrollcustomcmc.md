---
description: Crée une demande de certificat CMC et inscrit un ordinateur dans une hiérarchie de certificats.
ms.assetid: ef09ef04-8925-4d66-97ad-70b4d7cf78b9
title: enrollCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2910e6a6ca784aaeb9ca97dc8de106932bd64c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752733"
---
# <a name="enrollcustomcmc"></a>enrollCustomCMC

L’exemple enrollCustomCMC crée une demande de certificat CMC et inscrit un ordinateur dans une hiérarchie de certificats.

## <a name="location"></a>Emplacement

Lorsque vous installez le kit de développement logiciel (SDK) Microsoft Windows, l’exemple est installé, par défaut, dans le dossier *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ x509 Certificate \\ \\ enrollCustomCMC VC.

## <a name="discussion"></a>Discussions

Exemple enrollCustomCMC :

1.  Traite les arguments de ligne de commande suivants :
    -   Paire nom/valeur personnalisée à ajouter à la demande de certificat.
    -   Autre nom de l’objet.
    -   Identificateur d’objet (OID) pour l’extension d’utilisation améliorée de la clé.
2.  Crée un objet de requête [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) et l’initialise à l’aide du contexte de l’ordinateur.
3.  Utilise la \# requête PKCS 10 pour initialiser un objet [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .
4.  Crée un objet [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) à l’aide de l’OID spécifié sur la ligne de commande et l’ajoute à la collection d’extensions pour la demande CMC.
5.  Crée un objet [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) en utilisant le nom spécifié sur la ligne de commande, l’ajoute à la collection [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) , utilise la collection pour initialiser une extension [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) et l’ajoute à la collection d’extensions pour la demande CMC.
6.  Crée un objet [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) en utilisant le nom et la valeur spécifiés sur la ligne de commande et l’ajoute à la collection [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) sur la demande CMC.
7.  Crée un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , l’initialise à l’aide de l’objet de demande CMC et récupère une chaîne qui contient une demande encodée en base64.
8.  Crée un objet [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) et l’utilise pour récupérer une chaîne qui contient la configuration de l’autorité de certification.
9.  Crée un objet CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) et l’utilise, ainsi que les chaînes qui contiennent la configuration de l’autorité de certification et la demande de certificat pour envoyer la demande à l’autorité de certification.
10. Vérifie l’état de l’envoi et, en cas de réussite, installe le certificat dans le magasin de certificats.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Demande CMC](cmc-request.md)
</dt> <dt>

[\#Demande PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Utilisation des exemples inclus](using-the-included-samples.md)
</dt> </dl>

 

 
