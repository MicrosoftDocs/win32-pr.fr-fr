---
description: Inscrit un utilisateur final auprès d’une autorité de certification à l’aide d’un modèle, du nom de l’objet et de la longueur, en bits, de la clé.
ms.assetid: ee290c78-dbfa-4414-8489-aa886360652b
title: enrollSimpleUserCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4763e3ae68404e47207dccdb75c759fc30394e849bee07a71f2c54c649347a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119669909"
---
# <a name="enrollsimpleusercert"></a>enrollSimpleUserCert

L’exemple enrollSimpleUserCert inscrit un utilisateur final auprès d’une autorité de certification à l’aide d’un modèle, du nom de l’objet et de la longueur, en bits, de la clé.

## <a name="location"></a>Emplacement

lorsque vous installez le kit de développement logiciel (SDK) microsoft Windows, une version C++ de l’exemple est installée, par défaut, dans le dossier *% ProgramFiles%* \\ microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ Security \\ X509 certificate \\ \\ enrollSimpleUserCert VC. une version C# est installée dans le dossier *% ProgramFiles%* \\ Microsoft kits de développement logiciel (Windows sdk) \\ \\ EnrollSimpleUserCert v 7.0 \\ samples de l’inscription de \\ certificats X509 \\ CSharp \\ .

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

 

 



