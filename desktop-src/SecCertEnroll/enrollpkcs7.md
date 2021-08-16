---
description: Crée une \# demande PKCS 7 à partir d’un certificat existant en héritant des clés publiques et privées et du modèle de certificat.
ms.assetid: e7df1a2e-5674-4cc6-874b-45bcc7e25127
title: enrollPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0635fdf4daacc9c7a04db98c7e34e9d3495c6f18ca3e145b166f19e3cd49610a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117779950"
---
# <a name="enrollpkcs7"></a>enrollPKCS7

L’exemple enrollPKCS7 crée une \# demande PKCS 7 à partir d’un certificat existant en héritant des clés publiques et privées et du modèle de certificat. Le certificat existant est utilisé pour signer la demande. Cet exemple inscrit l’utilisateur dans une hiérarchie de certificats et installe la réponse du certificat. L’exemple utilise un certificat existant pour inscrire et installer un nouveau certificat. Pour plus d’informations sur le renouvellement d’un certificat existant, consultez [enrollRenewalPKCS7](enrollrenewalpkcs7.md).

## <a name="location"></a>Emplacement

lorsque vous installez le kit de développement logiciel (SDK) de microsoft Windows, l’exemple est installé, par défaut, dans le dossier *% ProgramFiles%* \\ microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ Security \\ X509 certificate \\ \\ enrollPKCS7 VC.

## <a name="discussion"></a>Discussions

Exemple enrollPKCS7 :

1.  Traite les arguments de ligne de commande. La ligne de commande doit contenir le nom du modèle de certificat utilisé pour rechercher un certificat existant.
2.  Récupère un certificat existant en utilisant le nom du modèle spécifié sur la ligne de commande ou, si un certificat est introuvable, tente d’inscrire un nouveau certificat créé à l’aide du modèle. Les fonctions findCertByTemplate et enrollCertByTemplate sont définies dans enrollCommon. cpp.
3.  Vérifie la chaîne de certificats et convertit le certificat en **BSTR**.
4.  Crée un objet [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) et l’initialise à l’aide du certificat existant. Le nouvel \# objet de requête PKCS 7 hérite des clés et du modèle privés et publics du certificat existant.
5.  Crée un objet [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , l’initialise à l’aide du certificat existant et l’ajoute à l’objet de \# requête PKCS 7.
6.  Crée un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , l’initialise à l’aide de l' \# objet de requête PKCS 7, tente de l’inscrire auprès de l’autorité de certification et surveille l’état du processus d’inscription. La fonction checkEnrollStatus est définie dans enrollCommon. cpp.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Demande CMC](cmc-request.md)
</dt> <dt>

[Utilisation des exemples inclus](using-the-included-samples.md)
</dt> </dl>

 

 



