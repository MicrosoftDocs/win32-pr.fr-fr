---
description: Inscrit un utilisateur final auprès d’une autorité de certification à l’aide d’un modèle, du nom de l’objet et de la longueur, en bits, de la clé.
ms.assetid: ee290c78-dbfa-4414-8489-aa886360652b
title: enrollSimpleUserCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0956455afa814af54cc86661f2d7733a6d16dd8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034738"
---
# <a name="enrollsimpleusercert"></a>enrollSimpleUserCert

L’exemple enrollSimpleUserCert inscrit un utilisateur final auprès d’une autorité de certification à l’aide d’un modèle, du nom de l’objet et de la longueur, en bits, de la clé.

## <a name="location"></a>Emplacement

Lorsque vous installez le kit de développement logiciel (SDK) Microsoft Windows, une version C++ de l’exemple est installée, par défaut, dans le dossier *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ x509 Certificate \\ \\ enrollSimpleUserCert VC. Une version C# est installée dans le dossier *% ProgramFiles%* \\ Microsoft kits de développement logiciel (SDK) \\ exemple d’inscription de \\ \\ \\ certificat x509 \\ \\ EnrollSimpleUserCert.

## <a name="discussion"></a>Discussions

Exemple enrollSimpleUserCert :

1.  Traite les arguments de ligne de commande. La ligne de commande doit contenir le nom du modèle, le nom de l’objet et la longueur de la clé.
2.  Crée un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) et l’initialise à l’aide du modèle.
3.  Récupère l’objet de demande de certificat interne à partir de l’objet d’inscription et l’interroge pour l’objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) . La requête la plus profonde est toujours une \# demande PKCS 10.
4.  Récupère l’objet [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) à partir de la \# demande PKCS 10 et définit la longueur de clé spécifiée sur la ligne de commande.
5.  Crée un objet [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , l’utilise pour encoder le nom d’objet X. 500 et ajoute le nom à la \# demande PKCS 10.
6.  Tente d’inscrire l’utilisateur final auprès de l’autorité de certification et surveille la progression du processus d’inscription. La fonction checkEnrollStatus est définie dans enrollCommon. cpp.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[\#Demande PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Utilisation des exemples inclus](using-the-included-samples.md)
</dt> </dl>

 

 



